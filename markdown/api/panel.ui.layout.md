# panel.ui.layout package

## Submodules

- [panel.ui.layout.modal module](panel.ui.layout.modal.md)
  - [Modal](panel.ui.layout.modal.md#panel.ui.layout.modal.Modal)
    - [Modal.create_button()](panel.ui.layout.modal.md#panel.ui.layout.modal.Modal.create_button)
    - [Modal.show()](panel.ui.layout.modal.md#panel.ui.layout.modal.Modal.show)
- [panel.ui.layout.widgetbox module](panel.ui.layout.widgetbox.md)
  - [WidgetBox](panel.ui.layout.widgetbox.md#panel.ui.layout.widgetbox.WidgetBox)

## Module contents

Material UI layouts, plus the classic layouts that have no Material
equivalent.

class panel.ui.layout.Accordion(\*objects, **params)
Bases: [MaterialNamedListLike](panel.ui.base.md#panel.ui.base.MaterialNamedListLike),
`PaperMixin`

The Accordion layout is a type of Card layout that allows switching
between multiple objects by clicking on the corresponding card header.

The labels for each card will default to the name parameter of the
card’s contents, but may also be defined explicitly as part of a tuple.

Accordion has a list-like API that allows interactively updating and
modifying the cards using the methods append, extend, clear, insert,
pop, remove and \_\_setitem\_\_.

References:

- [https://panel-material-ui.holoviz.org/reference/layouts/Accordion.html](https://panel-material-ui.holoviz.org/reference/layouts/Accordion.html)

- [https://panel.holoviz.org/reference/layouts/Accordion.html](https://panel.holoviz.org/reference/layouts/Accordion.html)

- [https://mui.com/material-ui/react-accordion/](https://mui.com/material-ui/react-accordion/)

Example:

\>\>\> Accordion(("Card 1", "Card 1 objects"), ("Card 2", "Card 2 objects"))\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> `panel_material_ui.layout.base.PaperMixin`:
> elevation, raised, square, variant
>
> [class="reference internal" title="panel.layout.base.NamedListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.NamedListLike](panel.layout.base.md#panel.layout.base.NamedListLike):
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
> title="panel_material_ui.layout.base.MaterialNamedListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialNamedListLike](panel.ui.base.md#panel.ui.base.MaterialNamedListLike):
> \_names, \_headers
>
>

`active_header_color`` ``=`` ``Color(allow_None=True,`` ``allow_named=True,`` ``label='Active`` ``header`` ``color')`
The text color of the active Card header.

`active_header_background`` ``=`` ``Color(allow_None=True,`` ``allow_named=True,`` ``label='Active`` ``header`` ``background')`
The background color of the active Card header.

`active`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Active')`
List of indexes of active cards.

`disabled`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Disabled')`
List of indexes of disabled cards.

`disable_gutters`` ``=`` ``Boolean(default=False,`` ``label='Disable`` ``gutters')`
Whether to disable margins between expanded sections.

`header_background`` ``=`` ``Color(allow_None=True,`` ``allow_named=True,`` ``label='Header`` ``background')`
The background color of the Card header.

`header_color`` ``=`` ``Color(allow_None=True,`` ``allow_named=True,`` ``label='Header`` ``color')`
The text color of the Card header.

`title_variant`` ``=`` ``String(default='h3',`` ``label='Title`` ``variant')`
The text variant of the Accordion header titles.

`toggle`` ``=`` ``Boolean(default=False,`` ``label='Toggle')`
Whether to toggle between active cards or allow multiple cards

class panel.ui.layout.Alert(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike)

An Alert displays messages, such as warnings, errors, success messages,
or informational updates. It provides a visually distinct way to inform
users about the system’s status.

References:

- [https://panel-material-ui.holoviz.org/reference/global/Notifications.html](https://panel-material-ui.holoviz.org/reference/global/Notifications.html)

- [https://mui.com/material-ui/react-alert/](https://mui.com/material-ui/react-alert/)

Example:

\>\>\> Alert(title="This is an alert")\

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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

`alert_type`` ``=`` ``Selector(default='primary',`` ``label='Alert`` ``type',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The type of the alert.

`closed`` ``=`` ``Boolean(default=False,`` ``label='Closed')`
Whether the alert is closed.

`closeable`` ``=`` ``Boolean(default=False,`` ``label='Closeable')`
Whether the alert is closeable.

`severity`` ``=`` ``Selector(default='success',`` ``label='Severity',`` ``names={},`` ``objects=['error',`` ``'warning',`` ``'info',`` ``'success'])`
The severity of the alert.

`object`` ``=`` ``String(default='',`` ``label='Object')`
The object to display in the alert.

`title`` ``=`` ``String(allow_None=True,`` ``label='Title')`
The title of the alert.

`variant`` ``=`` ``Selector(default='outlined',`` ``label='Variant',`` ``names={},`` ``objects=['filled',`` ``'outlined'])`
The variant of the alert.

class panel.ui.layout.Backdrop(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike)

The Backdrop component can be used to create a semi-transparent overlay
over the application’s UI. It is often used to focus attention on a
specific part of the interface, such as during loading states or while a
modal dialog is open.

References:

- [https://panel-material-ui.holoviz.org/reference/layouts/Backdrop.html](https://panel-material-ui.holoviz.org/reference/layouts/Backdrop.html)

- [https://mui.com/material-ui/react-backdrop/](https://mui.com/material-ui/react-backdrop/)

Example:

\>\>\> close = Button(on_click=lambda \_: backdrop.param.update(open=False), label='Close')  \# type: ignore\
\>\>\> backdrop = Backdrop(LoadingIndicator(), close)\
\>\>\> button = Button(on_click=lambda \_: backdrop.param.update(open=True), label=f'Open {Backdrop.name}')\
\>\>\> pn.Column(button, backdrop).servable()\

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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

`open`` ``=`` ``Boolean(default=False,`` ``label='Open')`
Whether the backdrop is open.

class panel.ui.layout.Card(\*items: list\[Any \| tuple\[str, Any\]\], **params: Any)
Bases: [MaterialNamedListLike](panel.ui.base.md#panel.ui.base.MaterialNamedListLike),
`PaperMixin`

A Card layout allows arranging multiple panel objects in a collapsible,
vertical container with a header bar.

References:

- [https://panel-material-ui.holoviz.org/reference/layouts/Card.html](https://panel-material-ui.holoviz.org/reference/layouts/Card.html)

- [https://panel.holoviz.org/reference/layouts/Card.html](https://panel.holoviz.org/reference/layouts/Card.html)

- [https://mui.com/material-ui/react-card/](https://mui.com/material-ui/react-card/)

Example:

\>\>\> Card(some_widget, some_pane, some_python_object, title='Card')\

Methods

|  |  |
|----|----|
| [select](#panel.ui.layout.Card.select)(\[selector\]) | Iterates over the Viewable and any potential children in the applying the Selector. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> `panel_material_ui.layout.base.PaperMixin`:
> elevation, raised, square, variant
>
> [class="reference internal" title="panel.layout.base.NamedListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.NamedListLike](panel.layout.base.md#panel.layout.base.NamedListLike):
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
> title="panel_material_ui.layout.base.MaterialNamedListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialNamedListLike](panel.ui.base.md#panel.ui.base.MaterialNamedListLike):
> \_names, \_headers
>
>

`collapsed`` ``=`` ``Boolean(default=False,`` ``label='Collapsed')`
Whether the contents of the Card are collapsed.

`collapsible`` ``=`` ``Boolean(default=True,`` ``label='Collapsible')`
Whether the Card should be expandable and collapsible.

`header`` ``=`` ``Child(allow_None=True,`` ``class_=<class`` ``'panel.viewable.Viewable'>,`` ``label='Header')`
A Panel component to display in the header bar of the Card. Will
override the given title if defined.

`header_background`` ``=`` ``Color(allow_None=True,`` ``allow_named=True,`` ``label='Header`` ``background')`
The background color of the Card header.

`header_color`` ``=`` ``Color(allow_None=True,`` ``allow_named=True,`` ``label='Header`` ``color')`
The text color of the Card header.

`header_css_classes`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Header`` ``css`` ``classes')`
List of CSS classes to apply to CardHeader component.

`hide_header`` ``=`` ``Boolean(default=False,`` ``label='Hide`` ``header')`
Whether to hide the card header.

`outlined`` ``=`` ``Boolean(default=True,`` ``label='Outlined')`
Whether the card is outlined.

`title`` ``=`` ``String(default='',`` ``label='Title')`
A title to be displayed in the Card header, will be overridden by the
header if defined.

`title_css_classes`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Title`` ``css`` ``classes')`
List of CSS classes to apply to CardTitle component.

`title_variant`` ``=`` ``String(default='h3',`` ``label='Title`` ``variant')`
The text variant of the Card header title.

select(selector: type \| Callable\[\[Viewable\], bool\] \| None = None) → list\[Viewable\]
Iterates over the Viewable and any potential children in the applying
the Selector.

Parameters:
**selector: type or callable or None**
The selector allows selecting a subset of Viewables by declaring a type
or callable function to filter by.

Returns:
viewables: list(Viewable)

class panel.ui.layout.Column(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike)

The Column layout arranges its contents vertically.

Methods

|  |  |
|----|----|
| [on_click](#panel.ui.layout.Column.on_click)(callback) | Register a callback invoked when the scroll-to-latest button is clicked. |
| [scroll_to](#panel.ui.layout.Column.scroll_to)(index) | Scrolls to the child at the provided index. |

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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

`auto_scroll_limit`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Auto`` ``scroll`` ``limit')`
Max pixel distance from the latest object in the Column to activate
automatic scrolling upon update. Setting to 0 disables auto-scrolling.

`scroll_button_threshold`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Scroll`` ``button`` ``threshold')`
Min pixel distance from the latest object in the Column to display the
scroll button. Setting to 0 disables the scroll button.

`scroll_position`` ``=`` ``Integer(default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Scroll`` ``position')`
Current scroll position of the Column. Setting this value will update
the scroll position of the Column. Setting to 0 will scroll to the top.

`scroll_index`` ``=`` ``Integer(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Scroll`` ``index')`
Index of the object to scroll to. Setting this value will scroll the
Column to the object at the given index.

`view_latest`` ``=`` ``Boolean(default=False,`` ``label='View`` ``latest')`
Whether to scroll to the latest object on init. If not enabled the view
will be on the first object.

`scroll_button_click`` ``=`` ``Event(default=False,`` ``label='Scroll`` ``button`` ``click')`
Triggered when the scroll-to-latest button is clicked.

on_click(callback: Callable\[\[Event\], None \| Awaitable\[None\]\]) → Watcher
Register a callback invoked when the scroll-to-latest button is clicked.

scroll_to(index: int)
Scrolls to the child at the provided index.

Parameters:
**index: int**
Index of the child object to scroll to.

class panel.ui.layout.Container(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike)

The Container layout centers your content horizontally. It’s the most
basic layout element.

References:

- [https://panel-material-ui.holoviz.org/reference/layouts/Container.html](https://panel-material-ui.holoviz.org/reference/layouts/Container.html)

- [https://mui.com/material-ui/react-container/](https://mui.com/material-ui/react-container/)

Example:

\>\>\> Container(some_widget, some_pane, some_python_object, title='Container')\

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
> width_policy, height_policy, visible
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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

`sizing_mode`` ``=`` ``Selector(allow_refs=True,`` ``default='stretch_width',`` ``label='Sizing`` ``mode',`` ``names={},`` ``objects=['fixed',`` ``'stretch_width',`` ``'stretch_height',`` ``'stretch_both',`` ``'scale_width',`` ``'scale_height',`` ``'scale_both',`` ``None])`
How the component should size itself. This is a high-level setting for
maintaining width and height of the component. To gain more fine grained
control over sizing, use `width_policy`,
`height_policy` and
`aspect_ratio` instead (those take precedence
over `sizing_mode`).
`"fixed"` Component is not responsive. It will
retain its original width and height regardless of any subsequent
browser window resize events. `"stretch_width"`
Component will responsively resize to stretch to the available width,
without maintaining any aspect ratio. The height of the component
depends on the type of the component and may be fixed or fit to
component’s contents. `"stretch_height"`
Component will responsively resize to stretch to the available height,
without maintaining any aspect ratio. The width of the component depends
on the type of the component and may be fixed or fit to component’s
contents. `"stretch_both"` Component is
completely responsive, independently in width and height, and will
occupy all the available horizontal and vertical space, even if this
changes the aspect ratio of the component.
`"scale_width"` Component will responsively
resize to stretch to the available width, while maintaining the original
or provided aspect ratio. `"scale_height"`
Component will responsively resize to stretch to the available height,
while maintaining the original or provided aspect ratio.
`"scale_both"` Component will responsively
resize to both the available width and height, while maintaining the
original or provided aspect ratio.

`disable_gutters`` ``=`` ``Boolean(default=False,`` ``label='Disable`` ``gutters')`
If True, the container will not have gutters.

`fixed`` ``=`` ``Boolean(default=False,`` ``label='Fixed')`
Set the max-width to match the min-width of the current breakpoint. This
is useful if you’d prefer to design for a fixed set of sizes instead of
trying to accommodate a fully fluid viewport.

`width_option`` ``=`` ``Selector(default='lg',`` ``label='Width`` ``option',`` ``names={},`` ``objects=['xs',`` ``'sm',`` ``'md',`` ``'lg',`` ``'xl',`` ``False])`
Width option for the container.

class panel.ui.layout.Details(\*items: list\[Any \| tuple\[str, Any\]\], **params: Any)
Bases: [MaterialNamedListLike](panel.ui.base.md#panel.ui.base.MaterialNamedListLike),
`PaperMixin`

A Details layout allows arranging multiple panel objects in a compact,
collapsible container with three expansion states: collapsed, expanded
(with scrollable area), and fully expanded.

References:

- [https://panel-material-ui.holoviz.org/reference/layouts/Details.html](https://panel-material-ui.holoviz.org/reference/layouts/Details.html)

Example:

\>\>\> Details(some_widget, some_pane, some_python_object, title='Details')\

Methods

|  |  |
|----|----|
| [select](#panel.ui.layout.Details.select)(\[selector\]) | Iterates over the Viewable and any potential children in the applying the Selector. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> `panel_material_ui.layout.base.PaperMixin`:
> elevation, raised, square, variant
>
> [class="reference internal" title="panel.layout.base.NamedListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.NamedListLike](panel.layout.base.md#panel.layout.base.NamedListLike):
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
> title="panel_material_ui.layout.base.MaterialNamedListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialNamedListLike](panel.ui.base.md#panel.ui.base.MaterialNamedListLike):
> \_names, \_headers
>
>

`collapsed`` ``=`` ``Boolean(default=True,`` ``label='Collapsed')`
Whether the contents of the Details are collapsed.

`fully_expanded`` ``=`` ``Boolean(default=False,`` ``label='Fully`` ``expanded')`
Whether the Details are fully expanded (no scrollable area). Only
applies when collapsed is False.

`header`` ``=`` ``Child(allow_None=True,`` ``class_=<class`` ``'panel.viewable.Viewable'>,`` ``label='Header')`
A Panel component to display in the header bar of the Details. Will
override the given title if defined.

`header_background`` ``=`` ``Color(allow_None=True,`` ``allow_named=True,`` ``label='Header`` ``background')`
The background color of the Details header.

`header_color`` ``=`` ``Color(allow_None=True,`` ``allow_named=True,`` ``label='Header`` ``color')`
The text color of the Details header.

`header_css_classes`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Header`` ``css`` ``classes')`
List of CSS classes to apply to DetailsHeader component.

`hide_header`` ``=`` ``Boolean(default=False,`` ``label='Hide`` ``header')`
Whether to hide the details header.

`outlined`` ``=`` ``Boolean(default=True,`` ``label='Outlined')`
Whether the details is outlined.

`scrollable_height`` ``=`` ``Integer(allow_None=True,`` ``default=150,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Scrollable`` ``height')`
Height of the scrollable area before it is fully expanded.

`title`` ``=`` ``String(default='',`` ``label='Title')`
A title to be displayed in the Details header, will be overridden by the
header if defined.

`title_css_classes`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Title`` ``css`` ``classes')`
List of CSS classes to apply to DetailsTitle component.

select(selector: type \| Callable\[\[Viewable\], bool\] \| None = None) → list\[Viewable\]
Iterates over the Viewable and any potential children in the applying
the Selector.

Parameters:
**selector: type or callable or None**
The selector allows selecting a subset of Viewables by declaring a type
or callable function to filter by.

Returns:
viewables: list(Viewable)

class panel.ui.layout.Dialog(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike)

The Dialog can be used to display important content in a modal-like
overlay that requires user interaction. It is often used for tasks such
as confirmations, forms, or displaying additional information.

References:

- [https://panel-material-ui.holoviz.org/reference/layouts/Dialog.html](https://panel-material-ui.holoviz.org/reference/layouts/Dialog.html)

- [https://mui.com/material-ui/react-dialog/](https://mui.com/material-ui/react-dialog/)

Example:

\>\>\> close = Button(on_click=lambda \_: dialog.param.update(open=False), label='Close')  \# type: ignore\
\>\>\> dialog = Dialog("This is a modal", close)\
\>\>\> button = Button(on_click=lambda \_: dialog.param.update(open=True), label=f'Open {Dialog.name}')\
\>\>\> pn.Column(button, dialog).servable()\

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
>

`scroll`` ``=`` ``Selector(default='paper',`` ``label='Scroll',`` ``names={},`` ``objects=['body',`` ``'paper'])`
Whether the dialog should scroll the content or the paper.

`close_on_click`` ``=`` ``Boolean(default=False,`` ``label='Close`` ``on`` ``click')`
Close when clicking outside the Dialog area.

`full_screen`` ``=`` ``Boolean(default=False,`` ``label='Full`` ``screen')`
Whether the dialog should be full screen.

`open`` ``=`` ``Boolean(default=False,`` ``label='Open')`
Whether the dialog is open.

`title`` ``=`` ``String(default='',`` ``label='Title')`
The title of the dialog.

`title_variant`` ``=`` ``String(default='h3',`` ``label='Title`` ``variant')`
The text variant of the Dialog title.

`show_close_button`` ``=`` ``Boolean(default=False,`` ``label='Show`` ``close`` ``button')`
Whether to show the close button.

`width_option`` ``=`` ``Selector(default='sm',`` ``label='Width`` ``option',`` ``names={},`` ``objects=['xs',`` ``'sm',`` ``'md',`` ``'lg',`` ``'xl',`` ``False])`
The width of the dialog.

class panel.ui.layout.Divider(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike)

A Divider draws a horizontal rule (a \<hr\> tag in HTML) to separate
multiple components in a layout.

References:

- [https://panel.holoviz.org/reference/layouts/Divider.html](https://panel.holoviz.org/reference/layouts/Divider.html)

- [https://mui.com/material-ui/react-divider/](https://mui.com/material-ui/react-divider/)

Example:

\>\>\> Divider(sizing_mode="stretch_width")\

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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

`orientation`` ``=`` ``Selector(default='horizontal',`` ``label='Orientation',`` ``names={},`` ``objects=['horizontal',`` ``'vertical'])`
Orientation of the divider.

`variant`` ``=`` ``Selector(default='fullWidth',`` ``label='Variant',`` ``names={},`` ``objects=['fullWidth',`` ``'inset',`` ``'middle'])`
Variant style of the divider.

class panel.ui.layout.Drawer(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike)

The Drawer component can be used to display important content in a
modal-like overlay that requires user interaction. It is often used for
tasks such as confirmations, forms, or displaying additional
information.

References:

- [https://panel-material-ui.holoviz.org/reference/layouts/Drawer.html](https://panel-material-ui.holoviz.org/reference/layouts/Drawer.html)

- [https://mui.com/material-ui/react-drawer/](https://mui.com/material-ui/react-drawer/)

Example:

\>\>\> drawer = Drawer("This is a drawer")\
\>\>\> button = Button(on_click=lambda \_: drawer.param.update(open=True), label='Open Drawer')\
\>\>\> pn.Column(button, drawer).servable()\

Methods

|  |  |
|----|----|
| [create_toggle](#panel.ui.layout.Drawer.create_toggle)(\[icon, active_icon\]) | Create a ToggleIcon for the drawer. |

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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

`anchor`` ``=`` ``Selector(default='left',`` ``label='Anchor',`` ``names={},`` ``objects=['left',`` ``'right',`` ``'top',`` ``'bottom'])`
Anchor position for the drawer.

`dock_icon`` ``=`` ``String(allow_None=True,`` ``label='Dock`` ``icon')`
Icon to display in the dock tab (only applies to ‘docked’ variant). When
unset, a directional chevron is used.

`dock_position`` ``=`` ``Selector(default='middle',`` ``label='Dock`` ``position',`` ``names={},`` ``objects=['start',`` ``'middle',`` ``'end'])`
Position of the toggle tab along the drawer edge (only applies to
‘docked’ variant).

`inline`` ``=`` ``Boolean(default=False,`` ``label='Inline')`
Whether the drawer is positioned inline within its parent container
rather than fixed/absolute to the page. When True, the drawer
participates in normal flow layout and pushes or shrinks sibling items.

`size`` ``=`` ``Integer(default=250,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Size')`
The width (for left/right anchors) or height (for top/bottom anchors) of
the drawer.

`open`` ``=`` ``Boolean(default=False,`` ``label='Open')`
Whether the drawer is open.

`variant`` ``=`` ``Selector(default='temporary',`` ``label='Variant',`` ``names={},`` ``objects=['docked',`` ``'permanent',`` ``'persistent',`` ``'temporary'])`
Variant style of the drawer.

create_toggle(icon: str = 'menu', active_icon: str = 'menu_open_icon', **params)
Create a ToggleIcon for the drawer.

Parameters:
**icon: str**
The icon to display when the drawer is closed.

**active_icon: str**
The icon to display when the drawer is open.

Returns:
toggle: ToggleIcon
A ToggleIcon component that can be used to toggle the drawer.

class panel.ui.layout.Feed(\*objects, **params)
Bases: [Column](#panel.ui.layout.Column)

The Feed layout is a buffered Column optimized for long, dynamic lists.

Methods

|  |  |
|----|----|
| [scroll_to_latest](#panel.ui.layout.Feed.scroll_to_latest)(\[scroll_limit\]) | Scrolls the Feed to the latest entry. |

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
> [title="panel_material_ui.layout.base.Column"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.Column](#panel.ui.layout.Column):
> auto_scroll_limit, scroll_button_threshold, scroll_position,
> scroll_index, view_latest, scroll_button_click
>
>

`scroll`` ``=`` ``Selector(default='y',`` ``label='Scroll',`` ``names={},`` ``objects=[False,`` ``True,`` ``'both-auto',`` ``'y-auto',`` ``'x-auto',`` ``'both',`` ``'x',`` ``'y'])`
Whether to add scrollbars if the content overflows the size of the
container. If “both-auto”, will only add scrollbars if the content
overflows in either directions. If “x-auto” or “y-auto”, will only add
scrollbars if the content overflows in the respective direction. If
“both”, will always add scrollbars. If “x” or “y”, will always add
scrollbars in the respective direction. If False, overflowing content
will be clipped. If True, will only add scrollbars in the direction of
the container, (e.g. Column: vertical, Row: horizontal).

`load_buffer`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=10,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Load`` ``buffer')`
The number of objects loaded on each side of the visible objects. When
scrolled halfway into the buffer, the feed will automatically load
additional objects while unloading objects on the opposite side.

`visible_children`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'str'>,`` ``label='Visible`` ``children')`
Internal list of currently visible frontend child model ids.

`visible_range`` ``=`` ``Range(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Visible`` ``range',`` ``length=2,`` ``readonly=True)`
Read-only upper and lower bounds of the currently visible feed objects.
This range is automatically updated based on scrolling.

scroll_to_latest(scroll_limit: float \| None = None) → None
Scrolls the Feed to the latest entry.

Parameters:
scroll_limit : float, optional
Maximum pixel distance from the latest object in the Feed to trigger
scrolling. If the distance exceeds this limit, scrolling will not occur.
If this is not set, it will always scroll to the latest while setting
this to 0 disables scrolling.

class panel.ui.layout.FlexBox(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike)

The FlexBox layout arranges its contents in a flex container.

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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

`align_content`` ``=`` ``Selector(default='flex-start',`` ``label='Align`` ``content',`` ``names={},`` ``objects=['normal',`` ``'flex-start',`` ``'flex-end',`` ``'center',`` ``'space-between',`` ``'space-around',`` ``'space-evenly',`` ``'stretch',`` ``'start',`` ``'end',`` ``'baseline',`` ``'first`` ``baseline',`` ``'last`` ``baseline'])`
Defines how a flex container’s lines align when there is extra space in
the cross-axis.

`align_items`` ``=`` ``Selector(default='flex-start',`` ``label='Align`` ``items',`` ``names={},`` ``objects=['stretch',`` ``'flex-start',`` ``'flex-end',`` ``'center',`` ``'baseline',`` ``'first`` ``baseline',`` ``'last`` ``baseline',`` ``'start',`` ``'end',`` ``'self-start',`` ``'self-end'])`
Defines the default behavior for how flex items are laid out along the
cross axis on the current line.

`flex_direction`` ``=`` ``Selector(default='row',`` ``label='Flex`` ``direction',`` ``names={},`` ``objects=['row',`` ``'row-reverse',`` ``'column',`` ``'column-reverse'])`
This establishes the main-axis, thus defining the direction flex items
are placed in the flex container.

`flex_wrap`` ``=`` ``Selector(default='wrap',`` ``label='Flex`` ``wrap',`` ``names={},`` ``objects=['nowrap',`` ``'wrap',`` ``'wrap-reverse'])`
Whether and how to wrap items in the flex container.

`gap`` ``=`` ``String(default='',`` ``label='Gap')`
Defines the spacing between flex items, supporting various units (px,
em, rem, %, vw/vh).

`justify_content`` ``=`` ``Selector(default='flex-start',`` ``label='Justify`` ``content',`` ``names={},`` ``objects=['flex-start',`` ``'flex-end',`` ``'center',`` ``'space-between',`` ``'space-around',`` ``'space-evenly',`` ``'start',`` ``'end',`` ``'left',`` ``'right'])`
Defines the alignment along the main axis.

class panel.ui.layout.FloatPanel(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike),
`PaperMixin`

A draggable, floating Paper surface for Panel and Material UI content.

Drag the empty surface to move the panel without blocking its children.
Position it relative to its parent or the viewport using named anchors.

Example:

\>\>\> FloatPanel("Content", position="center", contained=False)\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> `panel_material_ui.layout.base.PaperMixin`:
> elevation, raised, square, variant
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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

`contained`` ``=`` ``Boolean(default=True,`` ``label='Contained')`
Whether to position the panel within its parent rather than the
viewport.

`position`` ``=`` ``Selector(default='right-top',`` ``label='Position',`` ``names={},`` ``objects=['center',`` ``'left-top',`` ``'center-top',`` ``'right-top',`` ``'right-center',`` ``'right-bottom',`` ``'center-bottom',`` ``'left-bottom',`` ``'left-center'])`
Initial position within the parent or viewport.

`offsetx`` ``=`` ``Integer(default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Offsetx')`
Horizontal offset in pixels from the selected position.

`offsety`` ``=`` ``Integer(default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Offsety')`
Vertical offset in pixels from the selected position.

`controls`` ``=`` ``ListSelector(default=['minimize',`` ``'maximize',`` ``'close'],`` ``label='Controls',`` ``names={},`` ``objects=['minimize',`` ``'maximize',`` ``'close'])`
Title-bar controls to display. Set to an empty list to hide all
controls.

`status`` ``=`` ``Selector(default='normalized',`` ``label='Status',`` ``names={},`` ``objects=['normalized',`` ``'maximized',`` ``'minimized',`` ``'smallified',`` ``'smallifiedmax',`` ``'closed'])`
Current window state of the floating panel.

class panel.ui.layout.Grid(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike)

The Grid layout is a two-dimensional layout that allows arranging items
in a grid.

References:

- [https://panel-material-ui.holoviz.org/reference/layouts/Grid.html](https://panel-material-ui.holoviz.org/reference/layouts/Grid.html)

- [https://mui.com/material-ui/react-grid/](https://mui.com/material-ui/react-grid/)

Example:

\>\>\> Grid(some_widget, some_pane, some_python_object, title='Grid')\

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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

`container`` ``=`` ``Boolean(default=False,`` ``label='Container')`
Whether the grid should be a container.

`columns`` ``=`` ``ClassSelector(class_=(<class`` ``'int'>,`` ``<class`` ``'dict'>),`` ``default=12,`` ``label='Columns')`
The number of columns to display in the grid.

`column_spacing`` ``=`` ``Number(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Column`` ``spacing')`
The spacing between the columns in the grid. Overrides the spacing
parameter.

`direction`` ``=`` ``Selector(default='row',`` ``label='Direction',`` ``names={},`` ``objects=['row',`` ``'column',`` ``'column-reverse',`` ``'row-reverse'])`
Direction of grid arrangement.

`row_spacing`` ``=`` ``Number(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Row`` ``spacing')`
The spacing between the rows in the grid. Overrides the spacing
parameter.

`size`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'int'>,`` ``<class`` ``'str'>,`` ``<class`` ``'dict'>),`` ``label='Size')`
The size of the grid. Overrides the columns parameter.

`spacing`` ``=`` ``Number(default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Spacing')`
The spacing between the columns and rows in the grid.

class panel.ui.layout.GridBox(\*objects: Any, **params: Any)
Bases: [ListPanel](panel.layout.base.md#panel.layout.base.ListPanel)

The GridBox is a list-like layout (unlike GridSpec) that wraps objects
into a grid according to the specified nrows and ncols parameters.

It has a list-like API with methods to append, extend, clear, insert,
pop, remove and \_\_setitem\_\_, which makes it possible to
interactively update and modify the layout.

Reference:
[https://panel.holoviz.org/reference/layouts/GridBox.html](https://panel.holoviz.org/reference/layouts/GridBox.html)

Example:

\>\>\> pn.GridBox(\
...    python_object_1, python_object_2, ...,\
...    python_object_24, ncols=6\
... )\

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
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.layout.base.ListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.ListLike](panel.layout.base.md#panel.layout.base.ListLike):
> objects
>
> [class="reference internal" title="panel.layout.base.ListPanel"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.ListPanel](panel.layout.base.md#panel.layout.base.ListPanel):
> scroll
>
>

`nrows`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Nrows')`
Number of rows to reflow the layout into.

`ncols`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Ncols')`
Number of columns to reflow the layout into.

class panel.ui.layout.GridSpec(\*, mode, ncols, nrows, objects, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, name)
Bases: [Panel](panel.layout.base.md#panel.layout.base.Panel)

The GridSpec is an *array like* layout that allows arranging multiple
Panel objects in a grid using a simple API to assign objects to
individual grid cells or to a grid span.

Other layout containers function like lists, but a GridSpec has an API
similar to a 2D array, making it possible to use 2D assignment to
populate, index, and slice the grid.

See GridStack for a similar layout that allows the user to resize and
drag the cells.

Reference:
[https://panel.holoviz.org/reference/layouts/GridSpec.html](https://panel.holoviz.org/reference/layouts/GridSpec.html)

Example:

\>\>\> import panel as pn\
\>\>\> gspec = pn.GridSpec(width=800, height=600)\
\>\>\> gspec\[:,   0  \] = pn.Spacer(styles=dict(background='red'))\
\>\>\> gspec\[0,   1:3\] = pn.Spacer(styles=dict(background='green'))\
\>\>\> gspec\[1,   2:4\] = pn.Spacer(styles=dict(background='orange'))\
\>\>\> gspec\[2,   1:4\] = pn.Spacer(styles=dict(background='blue'))\
\>\>\> gspec\[0:1, 3:4\] = pn.Spacer(styles=dict(background='purple'))\
\>\>\> gspec\

Attributes:
**grid**

Methods

|  |  |
|----|----|
| [clone](#panel.ui.layout.GridSpec.clone)(**params) | Makes a copy of the GridSpec sharing the same parameters. |

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
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
>

`objects`` ``=`` ``ChildDict(class_=<class`` ``'dict'>,`` ``default={},`` ``label='Objects')`
The dictionary of child objects that make up the grid.

`mode`` ``=`` ``Selector(default='warn',`` ``label='Mode',`` ``names={},`` ``objects=['warn',`` ``'error',`` ``'override'])`
Whether to warn, error or simply override on overlapping assignment.

`ncols`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Ncols')`
Limits the number of columns that can be assigned.

`nrows`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Nrows')`
Limits the number of rows that can be assigned.

clone(**params)
Makes a copy of the GridSpec sharing the same parameters.

Parameters:
**params: Keyword arguments override the parameters on the clone.**

Returns:
Cloned GridSpec object

class panel.ui.layout.GridStack(\*, allow_drag, allow_resize, state, mode, ncols, nrows, objects, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, name)
Bases: [ReactiveHTML](panel.reactive.md#panel.reactive.ReactiveHTML),
[GridSpec](panel.layout.grid.md#panel.layout.grid.GridSpec)

The GridStack layout allows arranging multiple Panel objects in a grid
using a simple API to assign objects to individual grid cells or to a
grid span.

Other layout containers function like lists, but a GridSpec has an API
similar to a 2D array, making it possible to use 2D assignment to
populate, index, and slice the grid.

Reference:
[https://panel.holoviz.org/reference/layouts/GridStack.html](https://panel.holoviz.org/reference/layouts/GridStack.html)

Example:

\>\>\> pn.extension('gridstack')\
\>\>\> gstack = GridStack(sizing_mode='stretch_both')\
\>\>\> gstack\[ : , 0: 3\] = pn.Spacer(styles=dict(background='red'))\
\>\>\> gstack\[0:2, 3: 9\] = pn.Spacer(styles=dict(background='green'))\
\>\>\> gstack\[2:4, 6:12\] = pn.Spacer(styles=dict(background='orange'))\
\>\>\> gstack\[4:6, 3:12\] = pn.Spacer(styles=dict(background='blue'))\
\>\>\> gstack\[0:2, 9:12\] = pn.Spacer(styles=dict(background='purple'))\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, margin, styles, stylesheets, tags,
> width_policy, height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.layout.grid.GridSpec"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.grid.GridSpec](panel.layout.grid.md#panel.layout.grid.GridSpec):
> objects, mode, ncols, nrows
>
>

`height`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Height')`
The height of the component (in pixels). This can be either fixed or
preferred height, depending on height sizing policy.

`width`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
The width of the component (in pixels). This can be either fixed or
preferred width, depending on width sizing policy.

`allow_resize`` ``=`` ``Boolean(default=True,`` ``label='Allow`` ``resize')`
Allow resizing the grid cells.

`allow_drag`` ``=`` ``Boolean(default=True,`` ``label='Allow`` ``drag')`
Allow dragging the grid cells.

`state`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'dict'>,`` ``label='State')`
Current state of the grid (updated as items are resized and dragged).

class panel.ui.layout.HSpacer(refs=None, **params)
Bases: [Spacer](panel.layout.spacer.md#panel.layout.spacer.Spacer)

The HSpacer layout provides responsive horizontal spacing.

Using this component we can space objects equidistantly in a layout and
allow the empty space to shrink when the browser is resized.

How-to: [https://panel.holoviz.org/how_to/layout/spacing.html#spacer-components](https://panel.holoviz.org/how_to/layout/spacing.html#spacer-components)

Example:

\>\>\> pn.Row(\
...     pn.layout.HSpacer(), 'Item 1',\
...     pn.layout.HSpacer(), 'Item 2',\
...     pn.layout.HSpacer()\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, height, min_width,
> min_height, max_width, max_height, margin, styles, stylesheets, tags,
> width, width_policy, height_policy, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
>

`sizing_mode`` ``=`` ``Parameter(constant=True,`` ``default='stretch_width',`` ``label='Sizing`` ``mode',`` ``readonly=True)`
How the component should size itself. This is a high-level setting for
maintaining width and height of the component. To gain more fine grained
control over sizing, use `width_policy`,
`height_policy` and
`aspect_ratio` instead (those take precedence
over `sizing_mode`).
`"fixed"` Component is not responsive. It will
retain its original width and height regardless of any subsequent
browser window resize events. `"stretch_width"`
Component will responsively resize to stretch to the available width,
without maintaining any aspect ratio. The height of the component
depends on the type of the component and may be fixed or fit to
component’s contents. `"stretch_height"`
Component will responsively resize to stretch to the available height,
without maintaining any aspect ratio. The width of the component depends
on the type of the component and may be fixed or fit to component’s
contents. `"stretch_both"` Component is
completely responsive, independently in width and height, and will
occupy all the available horizontal and vertical space, even if this
changes the aspect ratio of the component.
`"scale_width"` Component will responsively
resize to stretch to the available width, while maintaining the original
or provided aspect ratio. `"scale_height"`
Component will responsively resize to stretch to the available height,
while maintaining the original or provided aspect ratio.
`"scale_both"` Component will responsively
resize to both the available width and height, while maintaining the
original or provided aspect ratio.

class panel.ui.layout.ListLike(\*objects: Any, **params: Any)
Bases: `Parameterized`

Methods

|  |  |
|----|----|
| [append](#panel.ui.layout.ListLike.append)(obj) | Appends an object to the layout. |
| [clear](#panel.ui.layout.ListLike.clear)() | Clears the objects on this layout. |
| [clone](#panel.ui.layout.ListLike.clone)(\*objects, **params) | Makes a copy of the layout sharing the same parameters. |
| [extend](#panel.ui.layout.ListLike.extend)(objects) | Extends the objects on this layout with a list. |
| [index](#panel.ui.layout.ListLike.index)(obj) | Returns the integer index of the supplied object in the list of objects. |
| [insert](#panel.ui.layout.ListLike.insert)(index, obj) | Inserts an object in the layout at the specified index. |
| [pop](#panel.ui.layout.ListLike.pop)(\[index\]) | Pops an item from the layout by index. |
| [remove](#panel.ui.layout.ListLike.remove)(obj) | Removes an object from the layout. |
| [reverse](#panel.ui.layout.ListLike.reverse)() | Reverses the objects in the layout. |

**Parameter Definitions**

------------------------------------------------------------------------

`objects`` ``=`` ``Children(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'panel.viewable.Viewable'>,`` ``label='Objects')`
The list of child objects that make up the layout.

append(obj: Any) → None
Appends an object to the layout.

Parameters:
**obj (object): Panel component to add to the layout.**

clear() → list\[Viewable\]
Clears the objects on this layout.

Returns:
objects (list\[Viewable\]): List of cleared objects.

clone(\*objects: t.Any, **params: t.Any) → Self
Makes a copy of the layout sharing the same parameters.

Parameters:
**objects: Objects to add to the cloned layout.**

**params: Keyword arguments override the parameters on the clone.**

Returns:
Cloned layout object

extend(objects: Iterable\[Any\]) → None
Extends the objects on this layout with a list.

Parameters:
**objects (list): List of panel components to add to the layout.**

index(obj: Viewable) → int
Returns the integer index of the supplied object in the list of objects.

Parameters:
**obj (Viewable): Panel component to look up the index for.**

Returns:
index (int): Integer index of the object in the layout.

insert(index: int, obj: Any) → None
Inserts an object in the layout at the specified index.

Parameters:
**index (int): Index at which to insert the object.**

**object (object): Panel components to insert in the layout.**

pop(index: int = -1) → Viewable
Pops an item from the layout by index.

Parameters:
**index (int): The index of the item to pop from the layout.**

remove(obj: Viewable) → None
Removes an object from the layout.

Parameters:
**obj (object): The object to remove from the layout.**

reverse() → None
Reverses the objects in the layout.

class panel.ui.layout.ListPanel(\*objects: Any, **params: Any)
Bases: [ListLike](panel.layout.base.md#panel.layout.base.ListLike),
[Panel](panel.layout.base.md#panel.layout.base.Panel)

An abstract baseclass for Panel objects with list-like children.

Methods

|  |  |
|----|----|
| [clone](#panel.ui.layout.ListPanel.clone)(\*objects, **params) | Makes a copy of the layout sharing the same parameters. |

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
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.layout.base.ListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.ListLike](panel.layout.base.md#panel.layout.base.ListLike):
> objects
>
>

`scroll`` ``=`` ``Selector(default=False,`` ``label='Scroll',`` ``names={},`` ``objects=[False,`` ``True,`` ``'both-auto',`` ``'y-auto',`` ``'x-auto',`` ``'both',`` ``'x',`` ``'y'])`
Whether to add scrollbars if the content overflows the size of the
container. If “both-auto”, will only add scrollbars if the content
overflows in either directions. If “x-auto” or “y-auto”, will only add
scrollbars if the content overflows in the respective direction. If
“both”, will always add scrollbars. If “x” or “y”, will always add
scrollbars in the respective direction. If False, overflowing content
will be clipped. If True, will only add scrollbars in the direction of
the container, (e.g. Column: vertical, Row: horizontal).

clone(\*objects: Any, **params: Any)
Makes a copy of the layout sharing the same parameters.

Parameters:
**objects: Objects to add to the cloned layout.**

**params: Keyword arguments override the parameters on the clone.**

Returns:
Cloned layout object

class panel.ui.layout.Modal(\*objects, **params)
Bases: [Dialog](#panel.ui.layout.Dialog)

A modal dialog that can be opened and closed, implemented by the
Material Dialog but keeping the classic Modal defaults and methods.

Example:

\>\>\> modal = Modal('Some content')\
\>\>\> Column(modal.create_button('show', label='Open'), modal)\

Methods

|  |  |
|----|----|
| [create_button](#panel.ui.layout.Modal.create_button)(action, **kwargs) | Create a button to show, hide or toggle the modal. |
| [show](#panel.ui.layout.Modal.show)() | Starts a Bokeh server and displays the Viewable in a new tab. |

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
> [title="panel_material_ui.layout.base.Dialog"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.Dialog](#panel.ui.layout.Dialog):
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

class panel.ui.layout.Panel(refs=None, **params)
Bases: [Reactive](panel.reactive.md#panel.reactive.Reactive),
[SizingModeMixin](panel.layout.base.md#panel.layout.base.SizingModeMixin)

Abstract baseclass for a layout of Viewables.

Methods

|  |  |
|----|----|
| [get_root](#panel.ui.layout.Panel.get_root)(\[doc, comm, preprocess\]) | Returns the root model and applies pre-processing hooks |
| [select](#panel.ui.layout.Panel.select)(\[selector\]) | Iterates over the Viewable and any potential children in the applying the Selector. |

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
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
>

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

select(selector=None)
Iterates over the Viewable and any potential children in the applying
the Selector.

Parameters:
**selector: type or callable or None**
The selector allows selecting a subset of Viewables by declaring a type
or callable function to filter by.

Returns:
viewables: list(Viewable)

class panel.ui.layout.Paper(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike),
`PaperMixin`

Paper implements a container for displaying content on an elevated
surface.

References:

- [https://panel-material-ui.holoviz.org/reference/layouts/Paper.html](https://panel-material-ui.holoviz.org/reference/layouts/Paper.html)

- [https://mui.com/material-ui/react-paper/](https://mui.com/material-ui/react-paper/)

Example:

\>\>\> Paper(name="Paper", objects=\[1, 2, 3\], elevation=10, width=200, height=200)\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> `panel_material_ui.layout.base.PaperMixin`:
> elevation, raised, square, variant
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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

`margin`` ``=`` ``Margin(allow_None=True,`` ``allow_refs=True,`` ``default=0,`` ``label='Margin')`
The margin of the layout.

`direction`` ``=`` ``Selector(default='column',`` ``label='Direction',`` ``names={},`` ``objects=['row',`` ``'column',`` ``'column-reverse',`` ``'row-reverse'])`
Direction of content arrangement in the paper.

class panel.ui.layout.Popup(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike)

The Popup component displays content in an anchored overlay that
requires user interaction. It is commonly used for contextual menus,
confirmations, forms, or any UI element that should appear relative to
another component or screen position.

Reference: [https://mui.com/material-ui/react-menu/](https://mui.com/material-ui/react-menu/)

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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

`anchor_origin`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={'horizontal':`` ``'right',`` ``'vertical':`` ``'bottom'},`` ``label='Anchor`` ``origin')`

`anchor_position`` ``=`` ``XYCoordinates(allow_None=True,`` ``label='Anchor`` ``position',`` ``length=2)`

`close_on_click`` ``=`` ``Boolean(default=True,`` ``label='Close`` ``on`` ``click')`
Close when clicking outside the Popup area.

`enforce_focus`` ``=`` ``Boolean(default=True,`` ``label='Enforce`` ``focus')`
Whether to enforce focus on the Popup while it is open.

`hide_backdrop`` ``=`` ``Boolean(default=False,`` ``label='Hide`` ``backdrop')`
Whether to hide the backdrop when the Popup is open.

`elevation`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Elevation')`
Elevation of the paper surface.

`open`` ``=`` ``Boolean(default=False,`` ``label='Open')`
Whether the pop-up is open.

`transform_origin`` ``=`` ``Dict(allow_None=True,`` ``class_=<class`` ``'dict'>,`` ``label='Transform`` ``origin')`

class panel.ui.layout.Row(\*objects, **params)
Bases: [MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike)

The Row layout arranges its contents horizontally.

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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
>

class panel.ui.layout.Spacer(refs=None, **params)
Bases: [Reactive](panel.reactive.md#panel.reactive.Reactive)

The Spacer layout is a very versatile component which makes it easy to
put fixed or responsive spacing between objects.

Like all other components spacers support both absolute and responsive
sizing modes.

How-to: [https://panel.holoviz.org/how_to/layout/spacing.html#spacer-components](https://panel.holoviz.org/how_to/layout/spacing.html#spacer-components)

Example:

\>\>\> pn.Row(\
...    1, pn.Spacer(width=200),\
...    2, pn.Spacer(width=100),\
...    3\
... )\

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
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
>

class panel.ui.layout.Swipe(\*objects, **params)
Bases: [ListLike](panel.layout.base.md#panel.layout.base.ListLike),
[ReactiveHTML](panel.reactive.md#panel.reactive.ReactiveHTML)

The Swipe layout enables you to quickly compare two panels laid out on
top of each other with a part of the *before* panel shown on one side of
a slider and a part of the *after* panel shown on the other side.

Attributes:
**after**

**before**

Methods

|  |  |
|----|----|
| [clone](#panel.ui.layout.Swipe.clone)(\*objects, **params) | Makes a copy of the layout sharing the same parameters. |
| [select](#panel.ui.layout.Swipe.select)(\[selector\]) | Iterates over the Viewable and any potential children in the applying the Selector. |

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
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
>

`objects`` ``=`` ``Children(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'panel.viewable.Viewable'>,`` ``label='Objects')`
The list of child objects that make up the layout.

`slider_width`` ``=`` ``Integer(bounds=(0,`` ``25),`` ``default=5,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Slider`` ``width')`
The width of the slider in pixels

`slider_color`` ``=`` ``Color(allow_named=True,`` ``default='black',`` ``label='Slider`` ``color')`
The color of the slider

`start`` ``=`` ``Integer(bounds=(0,`` ``100),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Start')`
Limits the minimum percentage the swipe handler can be moved to.

`end`` ``=`` ``Integer(bounds=(0,`` ``100),`` ``default=100,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End')`
Limits the maximum percentage the swipe handler can be moved to.

`value`` ``=`` ``Integer(bounds=(0,`` ``100),`` ``default=50,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
The percentage of the *after* panel to show.

`_before`` ``=`` ``Parameter(allow_None=True,`` ``label='`` ``before')`

`_after`` ``=`` ``Parameter(allow_None=True,`` ``label='`` ``after')`

clone(\*objects: t.Any, **params: t.Any) → Self
Makes a copy of the layout sharing the same parameters.

Parameters:
**objects: Objects to add to the cloned layout.**

**params: Keyword arguments override the parameters on the clone.**

Returns:
Cloned layout object

select(selector=None)
Iterates over the Viewable and any potential children in the applying
the Selector.

Parameters:
**selector: type or callable or None**
The selector allows selecting a subset of Viewables by declaring a type
or callable function to filter by.

Returns:
viewables: list(Viewable)

class panel.ui.layout.Tabs(\*objects, **params)
Bases: [MaterialNamedListLike](panel.ui.base.md#panel.ui.base.MaterialNamedListLike)

The Tabs layout allows switching between multiple objects by clicking on
the corresponding tab header.

Tab labels may be defined explicitly as part of a tuple or will be
inferred from the name parameter of the tab’s contents.

Like Accordion, Tabs has a list-like API with methods to append, extend,
clear, insert, pop, remove and \_\_setitem\_\_, which make it possible
to interactively update and modify the tabs.

References:

- [https://panel-material-ui.holoviz.org/reference/layouts/Tabs.html](https://panel-material-ui.holoviz.org/reference/layouts/Tabs.html)

- [https://panel.holoviz.org/reference/layouts/Tabs.html](https://panel.holoviz.org/reference/layouts/Tabs.html)

- [https://mui.com/material-ui/react-tabs/](https://mui.com/material-ui/react-tabs/)

Example:

\>\>\> Tabs(("Tab 1", "Tab 1 objects"), ("Tab 2", "Card 2 objects"))\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.layout.base.NamedListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.NamedListLike](panel.layout.base.md#panel.layout.base.NamedListLike):
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
> title="panel_material_ui.layout.base.MaterialNamedListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialNamedListLike](panel.ui.base.md#panel.ui.base.MaterialNamedListLike):
> \_names, \_headers
>
>

`active`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Active')`
Index of the currently displayed objects.

`closable`` ``=`` ``Boolean(default=False,`` ``label='Closable')`
Whether to display an icon to allow closing and thereby removing a tab.

`centered`` ``=`` ``Boolean(default=False,`` ``label='Centered')`
Whether the tabs should be centered.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
Color of the tabs component.

`disabled`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'int'>,`` ``label='Disabled')`
List of indexes of disabled tabs.

`dynamic`` ``=`` ``Boolean(default=False,`` ``label='Dynamic')`
Whether the tab contents should be rendered dynamically, i.e. only when
the tab is active.

`tabs_location`` ``=`` ``ObjectSelector(default='above',`` ``label='Tabs`` ``location',`` ``names={},`` ``objects=['above',`` ``'below',`` ``'left',`` ``'right'])`
The location of the tabs relative to the tab contents.

`wrapped`` ``=`` ``Boolean(default=False,`` ``label='Wrapped')`
Whether the tab labels should be wrapped.

class panel.ui.layout.VSpacer(refs=None, **params)
Bases: [Spacer](panel.layout.spacer.md#panel.layout.spacer.Spacer)

The VSpacer layout provides responsive vertical spacing.

Using this component we can space objects equidistantly in a layout and
allow the empty space to shrink when the browser is resized.

Reference: [https://panel.holoviz.org/how_to/layout/spacing.html#spacer-components](https://panel.holoviz.org/how_to/layout/spacing.html#spacer-components)

Example:

\>\>\> pn.Column(\
...     pn.layout.VSpacer(), 'Item 1',\
...     pn.layout.VSpacer(), 'Item 2',\
...     pn.layout.VSpacer()\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, height, min_width,
> min_height, max_width, max_height, margin, styles, stylesheets, tags,
> width, width_policy, height_policy, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
>

`sizing_mode`` ``=`` ``Parameter(constant=True,`` ``default='stretch_height',`` ``label='Sizing`` ``mode',`` ``readonly=True)`
How the component should size itself. This is a high-level setting for
maintaining width and height of the component. To gain more fine grained
control over sizing, use `width_policy`,
`height_policy` and
`aspect_ratio` instead (those take precedence
over `sizing_mode`).
`"fixed"` Component is not responsive. It will
retain its original width and height regardless of any subsequent
browser window resize events. `"stretch_width"`
Component will responsively resize to stretch to the available width,
without maintaining any aspect ratio. The height of the component
depends on the type of the component and may be fixed or fit to
component’s contents. `"stretch_height"`
Component will responsively resize to stretch to the available height,
without maintaining any aspect ratio. The width of the component depends
on the type of the component and may be fixed or fit to component’s
contents. `"stretch_both"` Component is
completely responsive, independently in width and height, and will
occupy all the available horizontal and vertical space, even if this
changes the aspect ratio of the component.
`"scale_width"` Component will responsively
resize to stretch to the available width, while maintaining the original
or provided aspect ratio. `"scale_height"`
Component will responsively resize to stretch to the available height,
while maintaining the original or provided aspect ratio.
`"scale_both"` Component will responsively
resize to both the available width and height, while maintaining the
original or provided aspect ratio.

class panel.ui.layout.WidgetBox(\*objects, **params)
Bases: [Paper](#panel.ui.layout.Paper)

The WidgetBox groups widgets on a Material Paper surface and, like the
classic WidgetBox, can disable all the widgets it contains.

Example:

\>\>\> WidgetBox(TextInput(label='Name'), Button(label='Submit'), disabled=True)\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> `panel_material_ui.layout.base.PaperMixin`:
> elevation, raised, square, variant
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
> title="panel_material_ui.layout.base.MaterialListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialListLike](panel.ui.base.md#panel.ui.base.MaterialListLike):
> scroll
>
> [title="panel_material_ui.layout.base.Paper"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.Paper](#panel.ui.layout.Paper):
> margin, direction
>
>

`disabled`` ``=`` ``Boolean(default=False,`` ``label='Disabled')`
Whether the widgets in the box are disabled.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
