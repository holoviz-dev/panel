# panel.ui.layout.modal module

A Material Dialog with the API of the classic Modal.

class panel.ui.layout.modal.Modal(\*objects, **params)
Bases: [Dialog](panel.ui.layout.md#panel.ui.layout.Dialog)

A modal dialog that can be opened and closed, implemented by the
Material Dialog but keeping the classic Modal defaults and methods.

Example:

\>\>\> modal = Modal('Some content')\
\>\>\> Column(modal.create_button('show', label='Open'), modal)\

Methods

|  |  |
|----|----|
| [create_button](#panel.ui.layout.modal.Modal.create_button)(action, **kwargs) | Create a button to show, hide or toggle the modal. |
| [show](#panel.ui.layout.modal.Modal.show)() | Starts a Bokeh server and displays the Viewable in a new tab. |

|            |     |
|------------|-----|
| **hide**   |     |
| **toggle** |     |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.layout.base.ListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.ListLike](panel.layout.base.md#panel.layout.base.ListLike):
> objects
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, height, min_width,
> min_height, max_width, max_height, styles, stylesheets, tags, width,
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
> title="panel_material_ui.layout.base.MaterialLayout"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialLayout](panel.ui.base.md#panel.ui.base.MaterialLayout):
> margin
>
> [class="reference internal"
> title="panel_material_ui.layout.base.Dialog"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.Dialog](panel.ui.layout.md#panel.ui.layout.Dialog):
> scroll, full_screen, open, title, title_variant, width_option
>
>

`close_on_click`` ``=`` ``Boolean(default=True,`` ``label='Close`` ``on`` ``click')`
Close when clicking outside the Dialog area.

`show_close_button`` ``=`` ``Boolean(default=True,`` ``label='Show`` ``close`` ``button')`
Whether to show a close button in the modal.

`background_close`` ``=`` ``Boolean(default=True,`` ``label='Background`` ``close')`
Whether to enable closing the modal when clicking the background. Alias
of close_on_click.

create_button(action: Literal\['show', 'hide', 'toggle'\], **kwargs) → Button
Create a button to show, hide or toggle the modal.

show()
Starts a Bokeh server and displays the Viewable in a new tab.

Parameters:
title : str \| None
A string title to give the Document (if served as an app)

**port: int (optional, default=0)**
Allows specifying a specific port

address : str
The address the server should listen on for HTTP requests.

**websocket_origin: str or list(str) (optional)**
A list of hosts that can connect to the websocket. This is typically
required when embedding a server app in an external web site. If None,
“localhost” is used.

**threaded: boolean (optional, default=False)**
Whether to launch the Server on a separate thread, allowing interactive
use.

**verbose: boolean (optional, default=True)**
Whether to print the address and port

open : boolean (optional, default=True)
Whether to open the server in a new browser tab

location : boolean or panel.io.location.Location
Whether to create a Location component to observe and set the URL
location.

Returns:
server: bokeh.server.Server or panel.io.server.StoppableThread
Returns the Bokeh server instance or the thread the server was launched
on (if threaded=True)

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
