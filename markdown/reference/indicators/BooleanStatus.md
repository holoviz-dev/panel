# BooleanStatus
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/indicators/BooleanStatus.ipynb)

------------------------------------------------------------------------

import panel as pn\
\
pn.extension()\

The `BooleanStatus` is a boolean indicator
providing a visual representation of a boolean status as filled or
non-filled circle. If the `value` is set to
`True` the indicator will be filled while
setting it to `False` will cause it to be
non-filled.

## Parameters:

For details on other options for customizing the component see the
[layout](../../../how_to/layout/index.md)
and [styling](../../../how_to/styling/index.md)
how-to guides.

- **`color`** (str): The color of the circle,
  one of ‘primary’, ‘secondary’, ‘success’, ‘info’, ‘warn’, ‘danger’,
  ‘light’, ‘dark’

- **`value`** (int or None): Whether the status
  indicator is filled or not.

------------------------------------------------------------------------

The `BooleanStatus` widget can be instantiated
as either `False` or
`True`:

false_status = pn.indicators.BooleanStatus(value=False)\
true_status = pn.indicators.BooleanStatus(value=True)\
\
pn.Row(false_status, true_status)\

The `BooleanStatus` indicator also supports a
range of colors:

grid = pn.GridBox('', 'False', 'True', ncols=3)\
\
for color in pn.indicators.BooleanStatus.param.color.objects:\
    false = pn.indicators.BooleanStatus(width=50, height=50, value=False, color=color)\
    true = pn.indicators.BooleanStatus(width=50, height=50, value=True, color=color)\
    grid.extend((color, false, true))\
\
grid\

------------------------------------------------------------------------
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/indicators/BooleanStatus.ipynb)

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

[https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/indicators/BooleanStatus.ipynb](https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/indicators/BooleanStatus.ipynb)

On this page
