# Swipe
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/layouts/Swipe.ipynb)

------------------------------------------------------------------------

import panel as pn\
import pandas as pd\
\
pn.extension()\

The `Swipe` layout enables you to quickly
compare two panels laid out on top of each other with a part of the
*before* panel shown on one side of a slider and a part of the *after*
panel shown on the other side.

## Parameters:

- **`end`** (int): Limits the maximum
  percentage the swipe handler can be moved to.

- **`objects`** (list): The before and after
  components to lay out.

- **`start`** (int): Limits the minimum
  percentage the swipe handler can be moved to.

- **`value`** (int): The percentage of the
  *after* panel shown. Default is 50.

Styling-related parameters:

- **`slider_width`** (int): The width of the
  slider in pixels. Default is 12.

- **`slider_color`** (str): The color of the
  slider. Default is ‘black’.

For further layout and styling-related parameters see the
[Control the
size](../../../tutorials/basic/size.md), [Align
Content](../../../tutorials/basic/align.md) and [Style](../../../tutorials/basic/style.md)
tutorials.

------------------------------------------------------------------------

The `Swipe` layout accepts any two objects,
which must have identical sizing options to work as intended.

Here we compare two images of mean surface temperatures in 1945-1949 and
temperatures between 2015-2019:

gis_1945 = 'https://earthobservatory.nasa.gov/ContentWOC/images/globaltemp/global_gis_1945-1949.png'\
gis_2015 = 'https://earthobservatory.nasa.gov/ContentWOC/images/globaltemp/global_gis_2015-2019.png'\
\
pn.Swipe(gis_1945, gis_2015)\

The layout can compare any type of component, e.g. here we will compare
two violin plots:

import hvplot.pandas\
\
penguins = pd.read_csv('https://datasets.holoviz.org/penguins/v1/penguins.csv')\
\
pn.Swipe(\
    penguins\[penguins.species=='Chinstrap'\].hvplot.violin('bill_length_mm', color='#00cde1'),\
    penguins\[penguins.species=='Adelie'\].hvplot.violin('bill_length_mm', color='#cd0000'),\
    value=51\
)\

We may also limit the minimum and maximum percentage the swipe handle
can be dragged to using the `start` and
`stop` values:

pn.Swipe(f"\<code\>\|{'-'\*100}\|\</code\>", f"\<code\>\|{'='\*100}\|\</code\>", start=20, end=80)\

------------------------------------------------------------------------
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/layouts/Swipe.ipynb)

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

[https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/layouts/Swipe.ipynb](https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/layouts/Swipe.ipynb)

On this page
