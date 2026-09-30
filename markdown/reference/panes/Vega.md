# Vega
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/panes/Vega.ipynb)

------------------------------------------------------------------------

import pandas as pd\
import panel as pn\
\
pn.extension('vega')\

The `Vega` pane renders Vega-based plots
(including those from Altair) inside a panel. It optimizes plot
rendering by using binary serialization for any array data found in the
Vega/Altair object, providing significant speedups over the standard
JSON serialization employed by Vega natively. Note that to use the
`Vega` pane in the notebook, the Panel
extension must be loaded with ‘vega’ as an argument to ensure that
vega.js is initialized.

## Parameters:

For details on other options for customizing the component, see the
[layout](../../../how_to/layout/index.md)
and [styling](../../../how_to/styling/index.md)
how-to guides.

- **`debounce`** (int or dict): The debounce
  timeout to apply to selection events, either specified as a single
  integer value (in milliseconds) or a dictionary that declares a
  debounce value per event. Debouncing ensures that events are only
  dispatched N milliseconds after a user is done interacting with the
  plot.

- **`object`** (dict or altair Chart): Either a
  dictionary containing a Vega or Vega-Lite plot specification, or an
  Altair Chart.

- **`show_actions`** (boolean): Whether to show
  the chart actions menu, such as save, edit, etc.

- **`theme`** (str): A theme to apply to the
  plot. Must be one of ‘excel’, ‘ggplot2’, ‘quartz’, ‘vox’,
  ‘fivethirtyeight’, ‘dark’, ‘latimes’, ‘urbaninstitute’,
  ‘googlecharts’, ‘powerbi’, ‘carbonwhite’, ‘carbong10’, ‘carbong90’, or
  ‘carbong100’.

Readonly parameters:

- **`selection`** (Selection): The Selection
  object exposes parameters that reflect the selections declared on the
  plot into Python.

------------------------------------------------------------------------

The `Vega` pane supports both
[vega](https://vega.github.io/vega/docs/specification/) and
[vega-lite](https://vega.github.io/vega-lite/docs/spec.html)
specifications, which may be provided in raw form (i.e., a dictionary)
or by defining an `altair` plot.

------------------------------------------------------------------------

## Vega and Vega-lite

To display `vega` and
`vega-lite` specification simply construct a
`Vega` pane directly or pass it to
`pn.panel`:

vegalite = {\
  "\$schema": "https://vega.github.io/schema/vega-lite/v5.json",\
  "data": {"url": "https://raw.githubusercontent.com/vega/vega/master/docs/data/barley.json"},\
  "mark": "bar",\
  "encoding": {\
    "x": {"aggregate": "sum", "field": "yield", "type": "quantitative"},\
    "y": {"field": "variety", "type": "nominal"},\
    "color": {"field": "site", "type": "nominal"}\
  }\
}\
vgl_pane = pn.pane.Vega(vegalite, height=240)\
vgl_pane\

Like all other panes, the `Vega` pane
`object` can be updated, either in place and
triggering an update:

vegalite\['mark'\] = 'area'\
vgl_pane.param.trigger('object')\

or by replacing the `object` entirely:

vega_disasters = {\
  "\$schema": "https://vega.github.io/schema/vega-lite/v5.json",\
  "data": {\
    "url": "https://raw.githubusercontent.com/vega/vega/master/docs/data/disasters.csv"\
  },\
  "width": 600,\
  "height": 400,\
  "transform": \[\
    {"filter": "datum.Entity !== 'All natural disasters'"}\
  \],\
  "mark": {\
    "type": "circle",\
    "opacity": 0.8,\
    "stroke": "black",\
    "strokeWidth": 1\
  },\
  "encoding": {\
    "x": {\
        "field": "Year",\
        "type": "quantitative",\
        "axis": {"labelAngle": 90},\
        "scale": {"zero": False}\
    },\
    "y": {\
        "field": "Entity",\
        "type": "nominal",\
        "axis": {"title": ""}\
    },\
    "size": {\
      "field": "Deaths",\
      "type": "quantitative",\
      "legend": {"title": "Annual Global Deaths", "clipHeight": 30},\
      "scale": {"range": \[0, 5000\]}\
    },\
    "color": {"field": "Entity", "type": "nominal", "legend": None}\
  }\
}\
vgl_pane.object = vega_disasters\

Lets reset the plot back to the original:

vgl_pane.object = vegalite\

### Exporting

You can export the current Vega or Vega-Lite specification using the
pane’s `export` method.

Supported output formats include:

- ‘png’ (`Image`)

- ‘jpeg’ (`Image`)

- ‘svg’ (`SVG`)

- ‘pdf’ (`PDF`)

- ‘html’ (`HTML`)

- ‘url’ (`HTML` to Vega Editor)

- ‘scenegraph’ (`JSON`)

Requires `vl-convert`, i.e.
`pip`` ``install`` ``vl-convert-python`.

vgl_pane.export('svg')\

\<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" class="marks" width="1015" height="282" viewBox="0 0 1015 282"\>\<rect width="1015" height="282" fill="white"/\>\<g fill="none" stroke-miterlimit="4" transform="translate(105,5)"\>\<g class="mark-group role-frame root" role="graphics-object" aria-roledescription="group mark container"\>\<g transform="translate(0,0)"\>\<path class="background" aria-hidden="true" d="M0.5,0.5h800v240h-800Z" stroke="#ddd"/\>\<g\>\<g class="mark-group role-axis" aria-hidden="true"\>\<g transform="translate(0.5,240.5)"\>\<path class="background" aria-hidden="true" d="M0,0h0v0h0Z" pointer-events="none"/\>\<g\>\<g class="mark-rule role-axis-grid" pointer-events="none"\>\<line transform="translate(0,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(32,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(64,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(96,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(128,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(160,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(192,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(224,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(256,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(288,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(320,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(352,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(384,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(416,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(448,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(480,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(512,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(544,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(576,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(608,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(640,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(672,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(704,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(736,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(768,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\<line transform="translate(800,0)" x2="0" y2="-240" stroke="#ddd" stroke-width="1" opacity="1"/\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" pointer-events="none" display="none"/\>\</g\>\</g\>\<g class="mark-group role-axis" role="graphics-symbol" aria-roledescription="axis" aria-label="X-axis titled 'Sum of yield' for a linear scale with values from 0 to 500"\>\<g transform="translate(0.5,240.5)"\>\<path class="background" aria-hidden="true" d="M0,0h0v0h0Z" pointer-events="none"/\>\<g\>\<g class="mark-rule role-axis-tick" pointer-events="none"\>\<line transform="translate(0,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(32,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(64,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(96,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(128,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(160,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(192,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(224,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(256,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(288,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(320,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(352,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(384,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(416,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(448,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(480,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(512,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(544,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(576,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(608,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(640,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(672,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(704,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(736,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(768,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(800,0)" x2="0" y2="5" stroke="#888" stroke-width="1" opacity="1"/\>\</g\>\<g class="mark-text role-axis-label" pointer-events="none"\>\<text text-anchor="start" transform="translate(0,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>0\</text\>\<text text-anchor="middle" transform="translate(32,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>20\</text\>\<text text-anchor="middle" transform="translate(64,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>40\</text\>\<text text-anchor="middle" transform="translate(96,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>60\</text\>\<text text-anchor="middle" transform="translate(128,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>80\</text\>\<text text-anchor="middle" transform="translate(160,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>100\</text\>\<text text-anchor="middle" transform="translate(192,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>120\</text\>\<text text-anchor="middle" transform="translate(224.00000000000003,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>140\</text\>\<text text-anchor="middle" transform="translate(256,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>160\</text\>\<text text-anchor="middle" transform="translate(288,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>180\</text\>\<text text-anchor="middle" transform="translate(320,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>200\</text\>\<text text-anchor="middle" transform="translate(352,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>220\</text\>\<text text-anchor="middle" transform="translate(384,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>240\</text\>\<text text-anchor="middle" transform="translate(416,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>260\</text\>\<text text-anchor="middle" transform="translate(448.00000000000006,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>280\</text\>\<text text-anchor="middle" transform="translate(480,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>300\</text\>\<text text-anchor="middle" transform="translate(512,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>320\</text\>\<text text-anchor="middle" transform="translate(544,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>340\</text\>\<text text-anchor="middle" transform="translate(576,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>360\</text\>\<text text-anchor="middle" transform="translate(608,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>380\</text\>\<text text-anchor="middle" transform="translate(640,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>400\</text\>\<text text-anchor="middle" transform="translate(672,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>420\</text\>\<text text-anchor="middle" transform="translate(704,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>440\</text\>\<text text-anchor="middle" transform="translate(736,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>460\</text\>\<text text-anchor="middle" transform="translate(768,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>480\</text\>\<text text-anchor="end" transform="translate(800,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>500\</text\>\</g\>\<g class="mark-rule role-axis-domain" pointer-events="none"\>\<line transform="translate(0,0)" x2="800" y2="0" stroke="#888" stroke-width="1" opacity="1"/\>\</g\>\<g class="mark-text role-axis-title" pointer-events="none"\>\<text text-anchor="middle" transform="translate(400,30)" font-family="sans-serif" font-size="11px" font-weight="bold" fill="#000" opacity="1"\>Sum of yield\</text\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" pointer-events="none" display="none"/\>\</g\>\</g\>\<g class="mark-group role-axis" role="graphics-symbol" aria-roledescription="axis" aria-label="Y-axis titled 'variety' for a discrete scale with 10 values: Glabron, Manchuria, No. 457, No. 462, No. 475, ending with Wisconsin No. 38"\>\<g transform="translate(0.5,0.5)"\>\<path class="background" aria-hidden="true" d="M0,0h0v0h0Z" pointer-events="none"/\>\<g\>\<g class="mark-rule role-axis-tick" pointer-events="none"\>\<line transform="translate(0,12)" x2="-5" y2="0" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(0,36)" x2="-5" y2="0" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(0,60)" x2="-5" y2="0" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(0,84)" x2="-5" y2="0" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(0,108)" x2="-5" y2="0" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(0,132)" x2="-5" y2="0" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(0,156)" x2="-5" y2="0" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(0,180)" x2="-5" y2="0" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(0,204)" x2="-5" y2="0" stroke="#888" stroke-width="1" opacity="1"/\>\<line transform="translate(0,228)" x2="-5" y2="0" stroke="#888" stroke-width="1" opacity="1"/\>\</g\>\<g class="mark-text role-axis-label" pointer-events="none"\>\<text text-anchor="end" transform="translate(-7,15)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Glabron\</text\>\<text text-anchor="end" transform="translate(-7,39)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Manchuria\</text\>\<text text-anchor="end" transform="translate(-7,63)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>No. 457\</text\>\<text text-anchor="end" transform="translate(-7,87)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>No. 462\</text\>\<text text-anchor="end" transform="translate(-7,111)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>No. 475\</text\>\<text text-anchor="end" transform="translate(-7,135)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Peatland\</text\>\<text text-anchor="end" transform="translate(-7,159)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Svansota\</text\>\<text text-anchor="end" transform="translate(-7,183)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Trebi\</text\>\<text text-anchor="end" transform="translate(-7,207)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Velvet\</text\>\<text text-anchor="end" transform="translate(-7,231)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Wisconsin No. 38\</text\>\</g\>\<g class="mark-rule role-axis-domain" pointer-events="none"\>\<line transform="translate(0,0)" x2="0" y2="240" stroke="#888" stroke-width="1" opacity="1"/\>\</g\>\<g class="mark-text role-axis-title" pointer-events="none"\>\<text text-anchor="middle" transform="translate(-88.8076171875,120) rotate(-90) translate(0,-2)" font-family="sans-serif" font-size="11px" font-weight="bold" fill="#000" opacity="1"\>variety\</text\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" pointer-events="none" display="none"/\>\</g\>\</g\>\<g class="mark-group role-scope pathgroup" role="graphics-object" aria-roledescription="group mark container"\>\<g transform="translate(0,0)"\>\<path class="background" aria-hidden="true" d="M0,0h800v240h-800Z"/\>\<g\>\<g class="mark-area role-mark marks" role="graphics-object" aria-roledescription="area mark container"\>\<path aria-label="Sum of yield: 79.86666; variety: Glabron; site: University Farm" role="graphics-symbol" aria-roledescription="area mark" d="M491.467,12L472.373,36L527.787,60L502.507,84L468.96,108L520.907,132L445.92,156L575.573,180L494.56,204L569.227,228L445.547,228L387.84,204L470.56,180L345.813,156L423.573,132L381.493,108L403.04,84L416.267,60L386.133,36L363.68,12Z" fill="#54a24b"/\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" display="none"/\>\</g\>\<g transform="translate(0,0)"\>\<path class="background" aria-hidden="true" d="M0,0h800v240h-800Z"/\>\<g\>\<g class="mark-area role-mark marks" role="graphics-object" aria-roledescription="area mark container"\>\<path aria-label="Sum of yield: 92.93333; variety: Glabron; site: Waseca" role="graphics-symbol" aria-roledescription="area mark" d="M640.16,12L604.107,36L688.267,60L679.253,84L609.813,108L656.267,132L583.253,156L756.48,180L634.773,204L756.373,228L569.227,228L494.56,204L575.573,180L445.92,156L520.907,132L468.96,108L502.507,84L527.787,60L472.373,36L491.467,12Z" fill="#eeca3b"/\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" display="none"/\>\</g\>\<g transform="translate(0,0)"\>\<path class="background" aria-hidden="true" d="M0,0h800v240h-800Z"/\>\<g\>\<g class="mark-area role-mark marks" role="graphics-object" aria-roledescription="area mark container"\>\<path aria-label="Sum of yield: 63.9; variety: Glabron; site: Morris" role="graphics-symbol" aria-roledescription="area mark" d="M363.68,12L386.133,36L416.267,60L403.04,84L381.493,108L423.573,132L345.813,156L470.56,180L387.84,204L445.547,228L322.933,228L283.893,204L325.92,180L248.533,156L306.667,132L274.56,108L279.253,84L300.693,60L287.253,36L261.44,12Z" fill="#72b7b2"/\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" display="none"/\>\</g\>\<g transform="translate(0,0)"\>\<path class="background" aria-hidden="true" d="M0,0h800v240h-800Z"/\>\<g\>\<g class="mark-area role-mark marks" role="graphics-object" aria-roledescription="area mark container"\>\<path aria-label="Sum of yield: 64.3; variety: Glabron; site: Crookston" role="graphics-symbol" aria-roledescription="area mark" d="M102.88,12L116.64,36L128,60L126.56,84L121.973,108L106.933,132L97.76,156L142.027,180L117.44,204L137.227,228L0,228L0,204L0,180L0,156L0,132L0,108L0,84L0,60L0,36L0,12Z" fill="#4c78a8"/\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" display="none"/\>\</g\>\<g transform="translate(0,0)"\>\<path class="background" aria-hidden="true" d="M0,0h800v240h-800Z"/\>\<g\>\<g class="mark-area role-mark marks" role="graphics-object" aria-roledescription="area mark container"\>\<path aria-label="Sum of yield: 43.56666; variety: Glabron; site: Grand Rapids" role="graphics-symbol" aria-roledescription="area mark" d="M261.44,12L287.253,36L300.693,60L279.253,84L274.56,108L306.667,132L248.533,156L325.92,180L283.893,204L322.933,228L234.72,228L195.467,204L245.28,180L174.453,156L208.32,132L218.667,108L207.52,84L218.08,60L199.093,36L191.733,12Z" fill="#e45756"/\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" display="none"/\>\</g\>\<g transform="translate(0,0)"\>\<path class="background" aria-hidden="true" d="M0,0h800v240h-800Z"/\>\<g\>\<g class="mark-area role-mark marks" role="graphics-object" aria-roledescription="area mark container"\>\<path aria-label="Sum of yield: 55.53334; variety: Glabron; site: Duluth" role="graphics-symbol" aria-roledescription="area mark" d="M191.733,12L199.093,36L218.08,60L207.52,84L218.667,108L208.32,132L174.453,156L245.28,180L195.467,204L234.72,228L137.227,228L117.44,204L142.027,180L97.76,156L106.933,132L121.973,108L126.56,84L128,60L116.64,36L102.88,12Z" fill="#f58518"/\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" display="none"/\>\</g\>\</g\>\<g class="mark-group role-legend" role="graphics-symbol" aria-roledescription="legend" aria-label="Symbol legend titled 'site' for fill color with 6 values: Crookston, Duluth, Grand Rapids, Morris, University Farm, Waseca"\>\<g transform="translate(818,0)"\>\<path class="background" aria-hidden="true" d="M0,0h87v92h-87Z" pointer-events="none"/\>\<g\>\<g class="mark-group role-legend-entry"\>\<g transform="translate(0,16)"\>\<path class="background" aria-hidden="true" d="M0,0h0v0h0Z" pointer-events="none"/\>\<g\>\<g class="mark-group role-scope" role="graphics-object" aria-roledescription="group mark container"\>\<g transform="translate(0,0)"\>\<path class="background" aria-hidden="true" d="M0,0h86.0048828125v11h-86.0048828125Z" pointer-events="none" opacity="1"/\>\<g\>\<g class="mark-symbol role-legend-symbol" pointer-events="none"\>\<path transform="translate(6,6)" d="M5,0A5,5,0,1,1,-5,0A5,5,0,1,1,5,0" fill="#4c78a8" stroke-width="1.5" opacity="1"/\>\</g\>\<g class="mark-text role-legend-label" pointer-events="none"\>\<text text-anchor="start" transform="translate(16,9)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Crookston\</text\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" pointer-events="none" display="none"/\>\</g\>\<g transform="translate(0,13)"\>\<path class="background" aria-hidden="true" d="M0,0h86.0048828125v11h-86.0048828125Z" pointer-events="none" opacity="1"/\>\<g\>\<g class="mark-symbol role-legend-symbol" pointer-events="none"\>\<path transform="translate(6,6)" d="M5,0A5,5,0,1,1,-5,0A5,5,0,1,1,5,0" fill="#f58518" stroke-width="1.5" opacity="1"/\>\</g\>\<g class="mark-text role-legend-label" pointer-events="none"\>\<text text-anchor="start" transform="translate(16,9)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Duluth\</text\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" pointer-events="none" display="none"/\>\</g\>\<g transform="translate(0,26)"\>\<path class="background" aria-hidden="true" d="M0,0h86.0048828125v11h-86.0048828125Z" pointer-events="none" opacity="1"/\>\<g\>\<g class="mark-symbol role-legend-symbol" pointer-events="none"\>\<path transform="translate(6,6)" d="M5,0A5,5,0,1,1,-5,0A5,5,0,1,1,5,0" fill="#e45756" stroke-width="1.5" opacity="1"/\>\</g\>\<g class="mark-text role-legend-label" pointer-events="none"\>\<text text-anchor="start" transform="translate(16,9)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Grand Rapids\</text\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" pointer-events="none" display="none"/\>\</g\>\<g transform="translate(0,39)"\>\<path class="background" aria-hidden="true" d="M0,0h86.0048828125v11h-86.0048828125Z" pointer-events="none" opacity="1"/\>\<g\>\<g class="mark-symbol role-legend-symbol" pointer-events="none"\>\<path transform="translate(6,6)" d="M5,0A5,5,0,1,1,-5,0A5,5,0,1,1,5,0" fill="#72b7b2" stroke-width="1.5" opacity="1"/\>\</g\>\<g class="mark-text role-legend-label" pointer-events="none"\>\<text text-anchor="start" transform="translate(16,9)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Morris\</text\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" pointer-events="none" display="none"/\>\</g\>\<g transform="translate(0,52)"\>\<path class="background" aria-hidden="true" d="M0,0h86.0048828125v11h-86.0048828125Z" pointer-events="none" opacity="1"/\>\<g\>\<g class="mark-symbol role-legend-symbol" pointer-events="none"\>\<path transform="translate(6,6)" d="M5,0A5,5,0,1,1,-5,0A5,5,0,1,1,5,0" fill="#54a24b" stroke-width="1.5" opacity="1"/\>\</g\>\<g class="mark-text role-legend-label" pointer-events="none"\>\<text text-anchor="start" transform="translate(16,9)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>University Farm\</text\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" pointer-events="none" display="none"/\>\</g\>\<g transform="translate(0,65)"\>\<path class="background" aria-hidden="true" d="M0,0h86.0048828125v11h-86.0048828125Z" pointer-events="none" opacity="1"/\>\<g\>\<g class="mark-symbol role-legend-symbol" pointer-events="none"\>\<path transform="translate(6,6)" d="M5,0A5,5,0,1,1,-5,0A5,5,0,1,1,5,0" fill="#eeca3b" stroke-width="1.5" opacity="1"/\>\</g\>\<g class="mark-text role-legend-label" pointer-events="none"\>\<text text-anchor="start" transform="translate(16,9)" font-family="sans-serif" font-size="10px" fill="#000" opacity="1"\>Waseca\</text\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" pointer-events="none" display="none"/\>\</g\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" pointer-events="none" display="none"/\>\</g\>\</g\>\<g class="mark-text role-legend-title" pointer-events="none"\>\<text text-anchor="start" transform="translate(0,9)" font-family="sans-serif" font-size="11px" font-weight="bold" fill="#000" opacity="1"\>site\</text\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" pointer-events="none" display="none"/\>\</g\>\</g\>\</g\>\<path class="foreground" aria-hidden="true" d="" display="none"/\>\</g\>\</g\>\</g\>\</svg\>

Additional kwargs may be passed to the
[vl-convert functions](https://github.com/jonmmease/vl-convert/tree/main).

To cast to a pane, use `as_pane=True`.

vgl_pane.export('png', scale=2, ppi=300, as_pane=True)\

### Responsive Sizing

The `vega-lite` specification can also be
responsively sized by declaring the width or height to match the
container:

responsive_spec = dict(vega_disasters, width='container', title="Responsive Plot")\
\
vgl_responsive_pane = pn.pane.Vega(responsive_spec)\
vgl_responsive_pane\

Please note that the `vega` specification does
not support setting `width` and
`height` to
`container`.

### DataFrame Data Values

For convenience we support a Pandas DataFrame as
`data` `values`:

dataframe_spec = {\
    "title": "A Simple Bar Chart from a Pandas DataFrame",\
    'config': {\
        'mark': {'tooltip': None},\
        'view': {'height': 200, 'width': 500}\
    },\
    'data': {'values': pd.DataFrame({'x': \['A', 'B', 'C', 'D', 'E'\], 'y': \[5, 3, 6, 7, 2\]})},\
    'mark': 'bar',\
    'encoding': {'x': {'type': 'ordinal', 'field': 'x'},\
                 'y': {'type': 'quantitative', 'field': 'y'}},\
    '\$schema': 'https://vega.github.io/schema/vega-lite/v3.2.1.json'\
}\
pn.pane.Vega(dataframe_spec)\

## Altair

A more convenient way of defining a Vega chart is to declare it using
[altair](https://altair-viz.github.io), which provides a declarative API
on top of vega-lite. The `Vega` pane will
automatically render the Vega-Lite spec when passed an Altair chart:

import altair as alt\
from vega_datasets import data\
\
cars = data.cars()\
\
chart = alt.Chart(cars).mark_circle(size=60).encode(\
    x='Horsepower',\
    y='Miles_per_Gallon',\
    color='Origin',\
    tooltip=\['Name', 'Origin', 'Horsepower', 'Miles_per_Gallon'\]\
).interactive()\
\
altair_pane = pn.panel(chart)\
altair_pane\

The Altair chart can also be updated by updating the pane
`object`:

altair_pane.object = chart.mark_circle(size=100)\

All the usual layouts and composition operators that Altair supports can
also be rendered:

penguins_url = "https://raw.githubusercontent.com/vega/vega/master/docs/data/penguins.json"\
\
chart1 = alt.Chart(penguins_url).mark_point().encode(\
    x=alt.X('Beak Length (mm):Q', scale=alt.Scale(zero=False)),\
    y=alt.Y('Beak Depth (mm):Q', scale=alt.Scale(zero=False)),\
    color='Species:N'\
).properties(\
    height=300,\
    width=300,\
)\
\
chart2 = alt.Chart(penguins_url).mark_bar().encode(\
    x='count()',\
    y=alt.Y('Beak Depth (mm):Q', bin=alt.Bin(maxbins=30)),\
    color='Species:N'\
).properties(\
    height=300,\
    width=100\
)\
\
pn.panel(chart1 \| chart2)\

## Selections

The `Vega` pane automatically syncs any
selections expressed on the Vega/Altair chart. Three types of selections
are currently supported:

- `selection_interval`: Allows selecting a
  intervals using a box-select tool, returns data in the form of
  `{<x-axis-name:`` ``[xmin,`` ``xmax],`` ``<y-axis-name>:`` ``[ymin,`` ``ymax]}`

- `selection_single`: Allows selecting a single
  point using clicks, returns a list of integer indices

- `selection_multi`: Allows selecting a
  multiple points using (shift+) click, returns a list of integer
  indices.

### Interval selection

As an example we can add an Altair
`selection_interval` selection to our chart:

import pandas as pd\
\
df = pd.read_json(penguins_url)\
\
brush = alt.selection_interval(name='brush')  \# selection of type "interval"\
\
chart = alt.Chart(penguins_url).mark_point().encode(\
    x=alt.X('Beak Length (mm):Q', scale=alt.Scale(zero=False)),\
    y=alt.Y('Beak Depth (mm):Q', scale=alt.Scale(zero=False)),\
    color=alt.condition(brush, 'Species:N', alt.value('lightgray'))\
).properties(\
    width=250,\
    height=250\
).add_params(\
    brush\
)\
\
vega_pane = pn.pane.Vega(chart, debounce=10)\
\
vega_pane\

Note we specified a single `debounce` value, if
we declare multiple selections we can instead declare a debounce value
per named event by specifying it as a dictionary, e.g.
`debounce={'brush':`` ``10,`` ``...}`.

The named selection will now appear on the
`.selection` sub-object:

vega_pane.selection\

Selection(brush=None, name='Selection00153')

By inspecting the JSON representation of the Altair chart we can see how
to express these selections in vega(-lite):

chart.to_dict()\['params'\]\

\[{'name': 'brush', 'select': {'type': 'interval'}}\]

### Single & multi-selection

Both single and multi-selection return the indices of the selected data
as a list (in the case of single selection the list is always of length
0 or 1).

multi = alt.selection_point(name='multi')  \# selection of type "multi"\
\
multi_chart = alt.Chart(penguins_url).mark_point().encode(\
    x=alt.X('Beak Length (mm):Q', scale=alt.Scale(zero=False)),\
    y=alt.Y('Beak Depth (mm):Q', scale=alt.Scale(zero=False)),\
    color=alt.condition(multi, 'Species:N', alt.value('lightgray'))\
).properties(\
    width=250,\
    height=250\
).add_params(\
    multi\
)\
\
vega_multi = pn.pane.Vega(multi_chart, debounce=10)\
\
vega_multi\

The `multi` value is now available on the
`selection` object:

vega_multi.selection\

Selection(multi=\[\], name='Selection00158')

To apply the selection we can simply use the
`.iloc` method on the pandas DataFrame
containing our data (try tapping on one or more points above and
re-running the cell below):

df.iloc\[vega_multi.selection.multi\]\

|  | Species | Island | Beak Length (mm) | Beak Depth (mm) | Flipper Length (mm) | Body Mass (g) | Sex |
|----|----|----|----|----|----|----|----|

For more background see the
[Altair](https://altair-viz.github.io/user_guide/interactions.html) documentation on available
interactions.

### Filtering a table via a selection

To filter a table via a chart selection we’re first going to bind the
`brush` selection to a function which filters
the dataframe to display only the selected values in the table. To
achieve this, we need to know that the selection returns a dictionary in
the format
`{'column_name':`` ``[min,`` ``max]}`,
which for our Penguins examples can look like this:

{'Beak Length (mm)': \[51.824, 53.952\], 'Beak Depth (mm)': \[18.796, 18.904\]}\

To display the selected values in a table, we will use the selection
dictionary to construct a pandas query string that can be used with
`DataFrame.query()`. Finally we are returning
both the query string and the filtered table in a Column:

def filtered_table(selection):\
    if not selection:\
        return '## No selection'\
    query = ' & '.join(\
        f'{crange\[0\]:.3f} \<= \`{col}\` \<= {crange\[1\]:.3f}'\
        for col, crange in selection.items()\
    )\
    return pn.Column(\
        f'Query: {query}',\
        pn.pane.DataFrame(df.query(query), width=600, height=300)\
    )\
\
pn.Row(vega_pane, pn.bind(filtered_table, vega_pane.selection.param.brush))\

Note that this way of constructing the query string means that Panel
currently supports filtering the table via the max and min values of the
selection area but does not check whether there are actually points
present in this area of the chart.

### Filtering another chart via a selection

Altair already provides a syntax for filtering one chart based on the
selection in another, but one limitation is that these charts need to be
displayed in the same layout for the filtering to work. By using Panel
to filter one Altair chart based on another, we can place the charts
anywhere in our app and still have the filtering work as expected.

One way to filter a chart based on the selection in another chart, is to
to use the same approach as above and create the second chart with the
dataframe filtered via `.query`. Altair also
provides a way to do the filtering directly with the
`transform_filter` method instead of using
pandas. In the example below, we are constructing a [composed](https://vega.github.io/vega-lite/docs/predicate.html#composition) [range predicate](https://vega.github.io/vega-lite/docs/predicate.html#range-predicate) from our selection object
and passing it to the `transform_filter` method
of the second chart.

def bar_counts(selection):\
    if not selection:\
        return '## No selection'\
    range_predicate = {\
        'and': \[{\
            'field': key,\
            'range': \[selection\[key\]\[0\], selection\[key\]\[1\]\]\
        } for key in selection\]\
    }\
    return alt.Chart(penguins_url, width=220).mark_bar().encode(\
        x='count()',\
        y='Species:N',\
        color=alt.Color('Species:N', legend=None)\
    ).transform_filter(\
        range_predicate\
    )\
\
pn.Column(vega_pane, pn.bind(bar_counts, vega_pane.selection.param.brush))\

### Filtering categorical data via a selection

Selections on categorical columns (‘nominal’ and ‘ordinal’ in Altair)
return all the selected values in a list rather than just the min and
max of the selection interval. Therefore, we need to construct the query
string as follows:

query = ' & '.join(\[f'\`{col}\` in {values}' for col, values in selection.items()\])\

In the example below we first check the data type in the column and then
use either the categorical and quantitative query string as appropriate,
which allows us to filter on a combination on categorical and numerical
data.

chart = alt.Chart(df).mark_tick().encode(\
    x=alt.X('Beak Length (mm):Q', scale=alt.Scale(zero=False)),\
    y='Species:N',\
    color=alt.condition(brush, 'Species:N', alt.value('lightgray'))\
).add_params(\
    brush\
)\
\
def filtered_table(selection):\
    if not selection:\
        return '## No selection'\
    query = ' & '.join(\
        f'{values\[0\]} \<= \`{col}\` \<= {values\[1\]}'\
        if pd.api.types.is_numeric_dtype(df\[col\])\
        else f'\`{col}\` in {values}' \
        for col, values in selection.items()\
    )\
    return pn.Column(\
        f'Query: {query}',\
        pn.pane.DataFrame(df.query(query), width=600, height=300)\
    )\
\
\
vega_pane = pn.pane.Vega(chart, debounce=10)\
pn.Row(vega_pane, pn.bind(filtered_table, vega_pane.selection.param.brush))\

### Filtering temporal data via a selection

Selections on temporal columns return the max and min of the selection
interval, just as for quantitative data. However, these are returned as
a Unix timestamp in milliseconds by default and therefore need to be
converted to a pandas timestamp before they can be used in a query
string. We can do this using
`pd.to_datetime(value,`` ``unit="ms")`
as in the example below.

from vega_datasets import data\
\
temps = data.seattle_temps()\[:300\]\
\
brush = alt.selection_interval(name='brush')\
\
chart = alt.Chart(temps).mark_circle().encode(\
    x='date:T',\
    y=alt.Y('temp:Q', scale={'zero': False}),\
    color=alt.condition(brush, alt.value('coral'), alt.value('lightgray'))\
).properties(\
    width=500\
).add_params(\
    brush\
)\
\
def filtered_table(selection):\
    if not selection:\
        return '## No selection'\
    query = ' & '.join(\
        f'"{pd.to_datetime(values\[0\], unit="ms")}" \<= \`{col}\` \<= "{pd.to_datetime(values\[1\], unit="ms")}"'\
        if pd.api.types.is_datetime64_any_dtype(temps\[col\]) else f'{values\[0\]} \<= \`{col}\` \<= {values\[1\]}'\
        for col, values in selection.items()\
    )\
    return pn.Column(\
        f'Query: {query}',\
        pn.pane.DataFrame(temps.query(query), width=600, height=300)\
    )\
\
\
vega_pane = pn.pane.Vega(chart, debounce=10)\
pn.Row(vega_pane, pn.bind(filtered_table, vega_pane.selection.param.brush))\

## Controls

The `Vega` pane exposes a number of options
which can be changed from both Python and Javascript. Try out the effect
of these parameters interactively:

pn.Row(vgl_responsive_pane.controls(jslink=True), vgl_responsive_pane, sizing_mode="stretch_width")\

------------------------------------------------------------------------
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/panes/Vega.ipynb)

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

[https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/panes/Vega.ipynb](https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/panes/Vega.ipynb)

On this page
