# Tqdm
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/indicators/Tqdm.ipynb)

------------------------------------------------------------------------

import time\
\
import numpy as np\
import pandas as pd\
import panel as pn\
\
from panel.widgets import Tqdm\
\
pn.extension()\

The `Tqdm` indicator wraps the well known
[tqdm](https://github.com/tqdm/tqdm) progress
indicator and displays the progress towards some target. You can use it
in the notebook or in your Panel web app.

[https://github.com/tqdm/tqdm](https://github.com/tqdm/tqdm)

## Parameters:

- **`layout`** (Column or Row): The layout of
  the `progress` indicator and the
  `text_pane`.

- **`max`** (int): The maximum progress value.

- **`progress`** (Progress): The Progress
  indicator to display the progress on.

- **`text`** (int): The current text being
  output by tqdm.

- **`text_pane`** (Str): The Pane displaying
  the progress `text`.

- **`value`** (int or None): The current value
  towards the progress.

- **`write_to_console`** (bool): Whether or not
  to also write to the console, only works on server.

For details on other options for customizing the component see the
[layout](../../../how_to/layout/index.md)
and [styling](../../../how_to/styling/index.md)
how-to guides. For a general introduction to
`tqdm` and lots of examples checkout the
[tqdm
github page](https://github.com/tqdm/tqdm).

------------------------------------------------------------------------

To use the `Tqdm` indicator instantiate the
object and then use the resulting variable just like you would use
`tqdm.tqdm`, i.e. you can iterate over any
iterable:

tqdm = Tqdm()\
\
def run_loop(\*events, timeout=0.2):\
    for i in tqdm(range(0,10), desc="My loop bar", leave=True, colour='#666666'):\
        if pn.state.\_is_pyodide:\
            \# time.sleep does not work in pyodide\
            np.random.random((10**6, 30))  \
        else:\
            time.sleep(timeout)\
        \
tqdm\

Most of the [parameters supported by tqdm](https://github.com/tqdm/tqdm#parameters) can be
passed to the call method of the `Tqdm`
indicator.

Click the button below to see the progress bar update (if you viewing
this on a live kernel):

button = pn.widgets.Button(label="Run Loop", color="success")\
button.on_click(run_loop)\
button\

## Nesting

When nesting `Tqdm` indicators using the
`margin` parameter allows visually indicating
the level of nesting.

tqdm_outer = Tqdm()\
tqdm_inner = Tqdm(margin=(0, 0, 0, 20))\
\
def run_nested_loop(\*events, timeout=0.05):\
    for i in tqdm_outer(range(10)):\
        for j in tqdm_inner(range(10)):\
            if pn.state.\_is_pyodide:\
                \# time.sleep does not work in pyodide\
                np.random.random((10**6, 30))  \
            else:\
                time.sleep(timeout)\
            \
run_nested_loop(timeout=0.01)\
\
pn.Column(tqdm_outer, tqdm_inner)\

button = pn.widgets.Button(label="Run Nested Loop", color="success")\
button.on_click(run_nested_loop)\
button\

------------------------------------------------------------------------
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/indicators/Tqdm.ipynb)

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

[https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/indicators/Tqdm.ipynb](https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/indicators/Tqdm.ipynb)

On this page
