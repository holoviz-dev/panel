# panel.ui.template package

## Module contents

The Material UI page and its parts. `Page`
replaces the classic templates.

class panel.ui.template.AppBar(\*objects, **params)
Bases: [MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent)

The AppBar component renders a Material UI App Bar (top navigation bar).
It supports a title, icon, color theming, and can contain arbitrary
child components (buttons, menus, search fields, etc.) via the objects
parameter.

The AppBar is typically placed at the top of an application as a header,
either standalone or inside a Page component’s header slot.

References:

- [https://panel-material-ui.holoviz.org/reference/page/AppBar.html](https://panel-material-ui.holoviz.org/reference/page/AppBar.html)

- [https://mui.com/material-ui/react-app-bar/](https://mui.com/material-ui/react-app-bar/)

Example:

\>\>\> pmui.AppBar(title='My App', icon='menu', color='primary')\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, height, min_width,
> min_height, max_width, max_height, margin, styles, stylesheets, tags,
> width, width_policy, height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.custom.ReactComponent"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.custom.ReactComponent](panel.custom.md#panel.custom.ReactComponent):
> use_shadow_dom
>
> [class="reference internal"
> title="panel_material_ui.base.MaterialComponent"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.base.MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent):
> loading, dark_theme, theme_config, sx
>
>

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'inherit',`` ``'primary',`` ``'secondary',`` ``'transparent'])`
The color of the app bar.

`drawer_toggle`` ``=`` ``Child(allow_None=True,`` ``class_=<class`` ``'panel.viewable.Viewable'>,`` ``label='Drawer`` ``toggle')`

`enable_color_on_dark`` ``=`` ``Boolean(default=False,`` ``label='Enable`` ``color`` ``on`` ``dark')`
If True, the color prop is applied in dark mode too (by default,
Material Design suppresses app bar color in dark mode).

`icon`` ``=`` ``String(allow_None=True,`` ``label='Icon')`
Icon displayed at the start of the app bar. Typically a menu or
navigation icon.

`objects`` ``=`` ``Children(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'panel.viewable.Viewable'>,`` ``label='Objects')`
Components rendered inside the app bar toolbar.

`position`` ``=`` ``Selector(default='static',`` ``label='Position',`` ``names={},`` ``objects=['fixed',`` ``'absolute',`` ``'sticky',`` ``'static',`` ``'relative'])`
The CSS position of the app bar.

`title`` ``=`` ``String(allow_None=True,`` ``label='Title')`
Title text displayed in the app bar.

`variant`` ``=`` ``Selector(default='dense',`` ``label='Variant',`` ``names={},`` ``objects=['dense',`` ``'regular'])`
The toolbar variant. ‘dense’ produces a compact bar.

class panel.ui.template.BreakpointSwitcher(\*, breakpoint, large, media_query, small, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, name)
Bases: [MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent)

The BreakpointSwitcher component allows switching between two component
implementations based on the declared breakpoint or media_query.

References:

- [https://panel-material-ui.holoviz.org/reference/page/BreakpointSwitcher.html](https://panel-material-ui.holoviz.org/reference/page/BreakpointSwitcher.html)

Example:

\>\>\> BreakpointSwitcher(breakpoint='sm', small=..., large=...)\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, height, min_width,
> min_height, max_width, max_height, margin, styles, stylesheets, tags,
> width, width_policy, height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.custom.ReactComponent"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.custom.ReactComponent](panel.custom.md#panel.custom.ReactComponent):
> use_shadow_dom
>
> [class="reference internal"
> title="panel_material_ui.base.MaterialComponent"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.base.MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent):
> loading, dark_theme, theme_config, sx
>
>

`current`` ``=`` ``Parameter(allow_None=True,`` ``constant=True,`` ``label='Current',`` ``readonly=True)`
The current object.

`breakpoint`` ``=`` ``Selector(default='md',`` ``label='Breakpoint',`` ``names={},`` ``objects=['xs',`` ``'sm',`` ``'md',`` ``'lg',`` ``'xl'])`
Breakpoint at which switcher toggles between.

`media_query`` ``=`` ``String(allow_None=True,`` ``label='Media`` ``query')`
Media query to use for the breakpoint (takes precedence over
breakpoint).

`small`` ``=`` ``Child(allow_None=True,`` ``class_=<class`` ``'panel.viewable.Viewable'>,`` ``label='Small')`
Items rendered in the small breakpoint.

`large`` ``=`` ``Child(allow_None=True,`` ``class_=<class`` ``'panel.viewable.Viewable'>,`` ``label='Large')`
Items rendered in the large breakpoint.

class panel.ui.template.Page(\*, \_custom_theme, app_bar_width, busy_indicator, config, contextbar, contextbar_open, contextbar_resizable, contextbar_variant, contextbar_width, favicon, header, logo, main, main_width, meta, sidebar, sidebar_open, sidebar_resizable, sidebar_variant, sidebar_width, site_url, template, theme_toggle, title, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, name)
Bases: [MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent),
[ResourceComponent](panel.io.resources.md#panel.io.resources.ResourceComponent)

The Page component is the equivalent of a Template in Panel.

Unlike a Template the Page component is implemented entirely in
Javascript, making it possible to dynamically update components.

References:

- [https://panel-material-ui.holoviz.org/reference/page/Page.html](https://panel-material-ui.holoviz.org/reference/page/Page.html)

Example:

\>\>\> Page(main=\['# Content'\], title='My App')\

Methods

|  |  |
|----|----|
| [get_root](#panel.ui.template.Page.get_root)(\[doc, comm, preprocess\]) | Returns the root model and applies pre-processing hooks |
| [resolve_resources](#panel.ui.template.Page.resolve_resources)(\[cdn, extras\]) | Resolves the resources required for this component. |
| [save](#panel.ui.template.Page.save)(filename\[, title, resources, template, ...\]) | Saves Panel objects to file. |
| [server_doc](#panel.ui.template.Page.server_doc)(\[doc, title, location\]) | Returns a serveable bokeh Document with the panel attached |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, height, min_width,
> min_height, max_width, max_height, margin, styles, stylesheets, tags,
> width, width_policy, height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.custom.ReactComponent"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.custom.ReactComponent](panel.custom.md#panel.custom.ReactComponent):
> use_shadow_dom
>
> [class="reference internal"
> title="panel_material_ui.base.MaterialComponent"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.base.MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent):
> loading, dark_theme, theme_config, sx
>
>

`app_bar_width`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'int'>,`` ``<class`` ``'str'>,`` ``<class`` ``'dict'>),`` ``label='App`` ``bar`` ``width')`
Maximum width of the app bar (header) content. When set, the toolbar
content is clamped to this width and centered, aligning it with a
clamped main area. Accepts a number (interpreted as pixels), a CSS
length string (e.g. ‘70ch’, ‘60rem’, ‘90%’), or a dict mapping Material
UI breakpoints to widths (e.g. {‘xs’: ‘100%’, ‘md’: 720, ‘lg’: 960}),
where each value applies at that breakpoint and up. Defaults to None
(full width); when unset it follows
`main_width` so the header stays aligned with
the main content.

`busy`` ``=`` ``Boolean(constant=True,`` ``default=False,`` ``label='Busy',`` ``readonly=True)`
Whether the page is busy.

`busy_indicator`` ``=`` ``Selector(default='linear',`` ``label='Busy`` ``indicator',`` ``names={},`` ``objects=['circular',`` ``'linear',`` ``None])`
The type of busy indicator to show.

`config`` ``=`` ``ClassSelector(class_=<class`` ``'panel.config._base_config'>,`` ``constant=True,`` ``default=_base_config(css_files=[],`` ``js_files={},`` ``js_modules={},`` ``name='_base_config00117',`` ``raw_css=[]),`` ``label='Config')`
Configuration object declaring custom CSS and JS files to load
specifically for this template.

`contextbar`` ``=`` ``Children(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'panel.viewable.Viewable'>,`` ``label='Contextbar')`
Items rendered in the contextbar.

`contextbar_open`` ``=`` ``Boolean(default=False,`` ``label='Contextbar`` ``open')`
Whether the contextbar is open or closed.

`contextbar_resizable`` ``=`` ``Boolean(default=False,`` ``label='Contextbar`` ``resizable')`
Whether the contextbar can be resized by dragging.

`contextbar_variant`` ``=`` ``Selector(default='temporary',`` ``label='Contextbar`` ``variant',`` ``names={},`` ``objects=['persistent',`` ``'temporary',`` ``'permanent',`` ``'auto'])`
Whether the contextbar is persistent, a temporary drawer, a permanent
drawer, or automatically switches between the two based on screen size.

`contextbar_width`` ``=`` ``Integer(default=250,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Contextbar`` ``width')`
Width of the contextbar

`favicon`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'str'>,`` ``<class`` ``'pathlib.Path'>),`` ``label='Favicon')`
The favicon of the page.

`header`` ``=`` ``Children(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'panel.viewable.Viewable'>,`` ``label='Header')`
Items rendered in the header.

`main`` ``=`` ``Children(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'panel.viewable.Viewable'>,`` ``label='Main')`
Items rendered in the main area.

`main_width`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'int'>,`` ``<class`` ``'str'>,`` ``<class`` ``'dict'>),`` ``label='Main`` ``width')`
Maximum width of the main content area. When set, the main content is
clamped to this width and centered to improve readability. Accepts a
number (interpreted as pixels), a CSS length string (e.g. ‘70ch’,
‘60rem’, ‘90%’), or a dict mapping Material UI breakpoints to widths
(e.g. {‘xs’: ‘100%’, ‘md’: 720, ‘lg’: 960}), where each value applies at
that breakpoint and up. Defaults to None (full width).

`meta`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=<class`` ``'panel_material_ui.template.base.Meta'>,`` ``label='Meta')`
Meta tags and other HTML head elements.

`logo`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'str'>,`` ``<class`` ``'pathlib.Path'>,`` ``<class`` ``'dict'>),`` ``label='Logo')`
Logo to render in the header. Can be a string, a pathlib.Path, or a
dictionary with breakpoints as keys, e.g. {‘sm’: ‘logo_mobile.png’,
‘md’: ‘logo.png’} or themes as keys, e.g. {‘dark’: ‘logo_dark.png’,
‘light’: ‘logo.png’}.

`sidebar`` ``=`` ``Children(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'panel.viewable.Viewable'>,`` ``label='Sidebar')`
Items rendered in the sidebar.

`sidebar_open`` ``=`` ``Boolean(default=True,`` ``label='Sidebar`` ``open')`
Whether the sidebar is open or closed.

`sidebar_resizable`` ``=`` ``Boolean(default=True,`` ``label='Sidebar`` ``resizable')`
Whether the sidebar can be resized by dragging.

`sidebar_variant`` ``=`` ``Selector(default='auto',`` ``label='Sidebar`` ``variant',`` ``names={},`` ``objects=['persistent',`` ``'temporary',`` ``'permanent',`` ``'auto'])`
Whether the sidebar is persistent, a temporary drawer, a permanent
drawer, or automatically switches between the two based on screen size.

`sidebar_width`` ``=`` ``Integer(default=320,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Sidebar`` ``width')`
Width of the sidebar

`site_url`` ``=`` ``String(default='/',`` ``label='Site`` ``url')`
URL of the site and logo. Default is ‘/’.

`template`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'str'>,`` ``<class`` ``'pathlib.Path'>,`` ``<class`` ``'jinja2.environment.Template'>),`` ``label='Template')`
Overrides the default jinja2 template. Template can be provided as a
string, Path or jinja2.Template instance.

`theme_toggle`` ``=`` ``Boolean(default=True,`` ``label='Theme`` ``toggle')`
Whether to show a theme toggle button.

`title`` ``=`` ``String(default='',`` ``label='Title')`
Title of the application.

`_custom_theme`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='`` ``custom`` ``theme')`

get_root(doc: Document \| None = None, comm: Comm \| None = None, preprocess: bool = True) → Model
Returns the root model and applies pre-processing hooks

Parameters:
**doc: bokeh.Document**
Bokeh document the bokeh model will be attached to.

**comm: pyviz_comms.Comm**
Optional pyviz_comms when working in notebook

**preprocess: boolean (default=True)**
Whether to run preprocessing hooks

Returns:
Returns the bokeh model corresponding to this panel object

resolve_resources(cdn: bool \| t.Literal\['auto'\] = 'auto', extras: dict\[str, dict\[str, str\]\] \| None = None) → ResourcesType
Resolves the resources required for this component.

Parameters:
**cdn: bool \| Literal\[‘auto’\]**
Whether to load resources from CDN or local server. If set to ‘auto’
value will be automatically determine based on global settings.

**extras: dict\[str, dict\[str, str\]\] \| None**
Additional resources to add to the bundle. Valid resource types include
js, js_modules and css.

Returns:
Dictionary containing JS and CSS resources.

save(filename: str \| PathLike \| IO\[Any\], title: str \| None = None, resources: \| None = None, template: str \| Template \| None = None, template_variables: dict\[str, Any\] \| None = None, **kwargs) → None\[source\]
Saves Panel objects to file.

Parameters:
**filename: str or file-like object**
Filename to save the plot to

**title: string**
Optional title for the plot

**resources: bokeh resources**
One of the valid bokeh.resources (e.g. CDN or INLINE)

**template:**
passed to underlying io.save

**template_variables:**
passed to underlying io.save

**embed: bool**
Whether the state space should be embedded in the saved file.

**max_states: int**
The maximum number of states to embed

**max_opts: int**
The maximum number of states for a single widget

**embed_json: boolean (default=True)**
Whether to export the data to json files

**json_prefix: str (default=’’)**
Prefix for the auto-generated json directory

**save_path: str (default=’./’)**
The path to save json files to

**load_path: str (default=None)**
The path or URL the json files will be loaded from.

**progress: boolean (default=True)**
Whether to report progress

**embed_states: dict (default={})**
A dictionary specifying the widget values to embed for each widget

**as_png: boolean (default=None)**
To save as a .png. If None save_png will be true if filename is string
and ends with png.

server_doc(doc: Document \| None = None, title: str \| None = None, location: bool \| LocationAreaBase \| None = True) → Document
Returns a serveable bokeh Document with the panel attached

Parameters:
doc : bokeh.Document (optional)
The bokeh Document to attach the panel to as a root, defaults to
bokeh.io.curdoc()

title : str
A string title to give the Document

location : boolean or panel.io.location.Location
Whether to create a Location component to observe and set the URL
location.

Returns:
doc : bokeh.Document
The bokeh document the panel was attached to

class panel.ui.template.ThemeToggle(\*, color, theme, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget)

A toggle button to switch between light and dark themes.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, height, min_width,
> min_height, max_width, max_height, styles, stylesheets, tags,
> width_policy, height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.custom.ReactComponent"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.custom.ReactComponent](panel.custom.md#panel.custom.ReactComponent):
> use_shadow_dom
>
> [class="reference internal"
> title="panel_material_ui.base.MaterialComponent"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.base.MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent):
> loading, dark_theme, theme_config, sx
>
> [class="reference internal"
> title="panel_material_ui.widgets.base.MaterialWidget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets.base.MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget):
> label, margin, attached, description, disabled
>
>

`value`` ``=`` ``Boolean(allow_None=True,`` ``label='Value')`
Whether the theme toggle is on or off.

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
The width of the theme toggle.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['primary',`` ``'secondary'])`
The color of the theme toggle.

`theme`` ``=`` ``Selector(constant=True,`` ``label='Theme',`` ``names={},`` ``objects=['dark',`` ``'default'])`
The current theme.

`variant`` ``=`` ``Selector(default='icon',`` ``label='Variant',`` ``names={},`` ``objects=['icon',`` ``'switch'])`
Whether to render just an icon or a toggle

width = None

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
