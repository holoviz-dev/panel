```python
import panel as pn

import pandas as pd
import holoviews as hv

from sklearn.cluster import KMeans

pn.extension()

import hvplot.pandas  # noqa: F401
```

```python
penguins = pd.read_csv('https://datasets.holoviz.org/penguins/v1/penguins.csv').dropna()
cols = list(penguins.columns)[2:6]

x = pn.ui.Select(label='x', options=cols, sizing_mode="stretch_width", margin=10)
y = pn.ui.Select(label='y', options=cols, value='bill_depth_mm', sizing_mode="stretch_width")
n_clusters = pn.ui.IntSlider(label='n_clusters', start=2, end=5, value=3, sizing_mode="stretch_width", margin=10)

def cluster(data, n_clusters):
    kmeans = KMeans(n_clusters=n_clusters, n_init='auto')
    est = kmeans.fit(data)
    return est.labels_.astype('str')

def plot(x, y, n_clusters):
    penguins['labels'] = cluster(penguins.iloc[:, 2:6].values, n_clusters)
    centers = penguins.groupby('labels').mean(numeric_only=True)
    return (penguins.sort_values('labels').hvplot.scatter(
        x, y, c='labels', hover_cols=['species'], line_width=1, size=60, frame_width=400, frame_height=400
    ).opts(marker=hv.dim('species').categorize({'Adelie': 'square', 'Chinstrap': 'circle', 'Gentoo': 'triangle'})) * centers.hvplot.scatter(
        x, y, marker='x', color='black', size=400, padding=0.1, line_width=5
    ))

description = pn.ui.Markdown("""
This app applies *k-means clustering* on the Palmer Penguins dataset using scikit-learn, parameterizing the number of clusters and the variables to plot.
<br><br>
Each cluster is denoted by one color while the penguin species is indicated using markers:
<br><br>
● - Adelie, ■ - Chinstrap,  ▲ - Gentoo
<br><br>
By comparing the two we can assess the performance of the clustering algorithm.
<br><br>
Additionally the center of each cluster is marked with an `X`.
<br><br>
""", sizing_mode="stretch_width")

explanation = pn.ui.Markdown("""
**Species**

Adelie: ●\n
Chinstrap: ■\n
Gentoo: ▲
""", margin=(0, 10))

code = pn.ui.Markdown("""
```python
import panel as pn

pn.extension()

x = pn.ui.Select(label='x', options=cols)
y = pn.ui.Select(label='y', options=cols, value='bill_depth_mm')
n_clusters = pn.ui.IntSlider(label='n_clusters', start=2, end=5, value=3)

explanation = pn.ui.Markdown(...)

def plot(x, y, n_clusters):
    ...

interactive_plot = pn.bind(plot, x, y, n_clusters)

pn.ui.Row(
    pn.ui.WidgetBox(x, y, n_clusters, explanation),
    interactive_plot
)
```
""", width=800)

app = pn.ui.Tabs(
    ('APP',
        pn.ui.Row(
            pn.ui.WidgetBox(x, y, n_clusters, explanation, width=175, margin=10),
            pn.bind(plot, x, y, n_clusters),),
    ),
    ('CODE', code),
    ('DESCRIPTION', description),
    width=800
)

pn.ui.Row(
    pn.ui.HSpacer(),
    app,
    pn.ui.HSpacer(),
    sizing_mode='stretch_width'
).embed(max_opts=4, json=True, json_prefix='json')
```
