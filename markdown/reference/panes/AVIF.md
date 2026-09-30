# AVIF
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/panes/AVIF.ipynb)

------------------------------------------------------------------------

import panel as pn\
\
pn.extension()\

The `AVIF` pane embeds a
`.avif` image file in a panel if provided a
local path, or will link to a remote image if provided a URL.

## Parameters:

For details on other options for customizing the component see the
[layout](../../../how_to/layout/index.md)
and [styling](../../../how_to/styling/index.md)
how-to guides.

- **`alt_text`** (str, default=None): alt text
  to add to the image tag. The alt text is shown when a user cannot load
  or display the image.

- **`embed`** (boolean, default=False): If
  given a URL to an image this determines whether the image will be
  embedded as base64 or merely linked to.

- **`fixed_aspect`** (boolean, default=True):
  Whether the aspect ratio of the image should be forced to be equal.

- **`link_url`** (str, default=None): A link
  URL to make the image clickable and link to some other website.

- **`object`** (str or object): The string to
  display. If a non-string type is supplied the repr is displayed.

- **`styles`** (dict): Dictionary specifying
  CSS styles

------------------------------------------------------------------------

The `AVIF` pane can be pointed at any local or
remote `.avif` file. If given a URL starting
with `http` or
`https`, the `embed`
parameter determines whether the image will be embedded or linked to:

avif_pane = pn.pane.AVIF('https://assets.holoviz.org/panel/samples/avif_sample.avif')\
\
avif_pane\

We can scale the size of the image by setting a specific fixed
`width` or `height`:

avif_pane.clone(width=100)\

Alternatively we can scale the width and height using the
`sizing_mode`:

pn.pane.AVIF('https://assets.holoviz.org/panel/samples/avif_sample.avif', sizing_mode='stretch_width')\

Note that by default the aspect ratio of the image is fixed, and so
there may be a gap beside or below the image even in responsive sizing
modes. To override this behavior set
`fixed_aspect=False` or provide fixed
`width` and `height`
values.

------------------------------------------------------------------------
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/panes/AVIF.ipynb)

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

[https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/panes/AVIF.ipynb](https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/panes/AVIF.ipynb)

On this page
