# panel.ui.widgets package

## Submodules

- [panel.ui.widgets.debugger module](panel.ui.widgets.debugger.md)
  - [Debugger](panel.ui.widgets.debugger.md#panel.ui.widgets.debugger.Debugger)

## Module contents

Material UI widgets, plus the classic widgets that have no Material
equivalent.

class panel.ui.widgets.ArrayInput(\*, enter_pressed, max_length, size, color, error_state, helper_text, variant, attached, dark_theme, sx, theme_config, use_shadow_dom, max_array_size, description, placeholder, serializer, type, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [TextInput](#panel.ui.widgets.TextInput),
[ArrayInput](panel.widgets.input.md#panel.widgets.input.ArrayInput)

Edit NumPy arrays as text, disabling editing above
`max_array_size`.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal"
> title="panel.widgets.input.LiteralInput"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets. input .LiteralInput](panel.widgets.input.md#panel.widgets.input.LiteralInput):
> serializer, type
>
> [class="reference internal" title="panel.widgets.input.ArrayInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets. input .ArrayInput](panel.widgets.input.md#panel.widgets.input.ArrayInput):
> max_array_size
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._TextInputBase`:
> max_length, placeholder, size
>
> [title="panel_material_ui.widgets.input.TextInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets. input .TextInput](#panel.ui.widgets.TextInput):
> enter_pressed
>
>

`value`` ``=`` ``Parameter(allow_None=True,`` ``label='Value')`
The widget value which the widget type resolves to when used as a
reactive param reference.

`value_input`` ``=`` ``Parameter(allow_None=True,`` ``constant=True,`` ``label='Value`` ``input',`` ``readonly=True)`
Initial or entered text value updated on every key press.

value = None

value_input = None

class panel.ui.widgets.AutocompleteInput(\*, case_sensitive, color, error_state, helper_text, lazy_search, min_characters, placeholder, restrict, search_strategy, size, variant, attached, description, dark_theme, sx, theme_config, use_shadow_dom, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MaterialSingleSelectBase`

The AutocompleteInput widget allows searching and selecting a single
value from a list of options.

It falls into the broad category of single-value, option-selection
widgets that provide a compatible API and include the Select,
RadioBoxGroup and RadioButtonGroup widgets.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/AutocompleteInput.html](https://panel-material-ui.holoviz.org/reference/widgets/AutocompleteInput.html)

- [https://panel.holoviz.org/reference/widgets/AutocompleteInput.html](https://panel.holoviz.org/reference/widgets/AutocompleteInput.html)

- [https://mui.com/material-ui/react-autocomplete/](https://mui.com/material-ui/react-autocomplete/)

Example:

\>\>\> AutocompleteInput(\
...     label='Study', options=\['Biology', 'Chemistry', 'Physics'\],\
... )\

Methods

|  |  |
|----|----|
| [clone](#panel.ui.widgets.AutocompleteInput.clone)(**params) | Makes a copy of the object sharing the same parameters. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.select.MaterialSingleSelectBase`:
> value
>
>

`case_sensitive`` ``=`` ``Boolean(default=True,`` ``label='Case`` ``sensitive')`
Enable or disable case sensitivity.

`error_state`` ``=`` ``Boolean(default=False,`` ``label='Error`` ``state')`
Whether to display in error state.

`helper_text`` ``=`` ``String(default='',`` ``label='Helper`` ``text')`
Helper text displayed below the input field.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the autocomplete input.

`lazy_search`` ``=`` ``Boolean(default=False,`` ``label='Lazy`` ``search')`
If True, search queries are sent to the backend for processing. This is
useful when options are large or need server-side filtering.

`min_characters`` ``=`` ``Integer(default=2,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Min`` ``characters')`
The number of characters a user must type before completions are
presented.

`placeholder`` ``=`` ``String(default='',`` ``label='Placeholder')`
Placeholder for empty input field.

`restrict`` ``=`` ``Boolean(default=True,`` ``label='Restrict')`
Set to False in order to allow users to enter text that is not present
in the list of completion strings.

`search_strategy`` ``=`` ``Selector(default='starts_with',`` ``label='Search`` ``strategy',`` ``names={},`` ``objects=['starts_with',`` ``'includes'])`
Define how to search the list of completion strings. The default option
“starts_with” means that the user’s text must match the start of a
completion string. Using “includes” means that the user’s text can match
any substring of a completion string.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
Size of the input field. Options: - ‘small’: Compact size for dense
layouts - ‘medium’: Standard size (default for most use cases) -
‘large’: Larger size for more visibility

`value_input`` ``=`` ``Parameter(constant=True,`` ``default='',`` ``label='Value`` ``input',`` ``readonly=True)`
Initial or entered text value updated on every key press.

`variant`` ``=`` ``Selector(default='outlined',`` ``label='Variant',`` ``names={},`` ``objects=['filled',`` ``'outlined',`` ``'standard'])`
Variant style of the autocomplete input.

clone(**params) → Self
Makes a copy of the object sharing the same parameters.

Parameters:
**params: Keyword arguments override the parameters on the clone.**

Returns:
Cloned Viewable object

class panel.ui.widgets.Avatar(content=None, **params)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget)

The Avatar component displays profile pictures, user initials, or icons
in a compact, circular or square format. Avatars are commonly used
throughout user interfaces to represent users, brands, or entities in a
visually consistent manner.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/Avatar.html](https://panel-material-ui.holoviz.org/reference/widgets/Avatar.html)

- [https://mui.com/material-ui/react-avatar/](https://mui.com/material-ui/react-avatar/)

Example:

\>\>\> Avatar(content="JD", color="#2196f3", variant="square")\

Methods

|  |  |
|----|----|
| [js_on_click](#panel.ui.widgets.Avatar.js_on_click)(\[args, code\]) | Allows defining a JS callback to be triggered when the Avatar is clicked. |
| [on_click](#panel.ui.widgets.Avatar.on_click)(callback) | Register a callback to be executed when the Avatar is clicked. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> value
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

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of the widget.

`alt_text`` ``=`` ``String(allow_None=True,`` ``label='Alt`` ``text')`
Alternative text for the image. Shown when the image cannot be loaded
and used for accessibility.

`clicks`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Clicks')`
Number of clicks.

`color`` ``=`` ``Color(allow_None=True,`` ``allow_named=True,`` ``label='Color')`
Background color for text and icon avatars. Accepts any valid CSS color
value. Only applies to text/icon avatars, not image avatars.

`content`` ``=`` ``String(default='',`` ``label='Content')`
The content to display in the avatar. Can be an image URL/path for image
avatars, or text content (like initials) for text avatars.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
Size of the avatar component. Options: - ‘small’: 24x24 pixels -
‘medium’: 40x40 pixels - ‘large’: 56x56 pixels

`variant`` ``=`` ``Selector(default='rounded',`` ``label='Variant',`` ``names={},`` ``objects=['rounded',`` ``'square'])`
Shape variant of the avatar. Options: - ‘rounded’: Circular shape with
rounded corners (default) - ‘square’: Square shape with sharp corners

`object`` ``=`` ``Parameter(allow_None=True,`` ``label='Object')`

js_on_click(args: dict\[str, Any\] \| None = None, code: str = '') → Callback
Allows defining a JS callback to be triggered when the Avatar is
clicked.

Returns:
callback: Callback
The Callback which can be used to disable the callback.

on_click(callback: Callable\[\[Event\], None\]) → Watcher
Register a callback to be executed when the Avatar is clicked.

Returns:
watcher: param.Parameterized.Watcher
A Watcher that executes the callback when the Avatar is clicked.

width = None

class panel.ui.widgets.BooleanStatus(\*, color, throttle, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [BooleanIndicator](panel.widgets.indicators.md#panel.widgets.indicators.BooleanIndicator)

The BooleanStatus is a boolean indicator providing a visual
representation of a boolean status as filled or non-filled circle.

If the value is set to True the indicator will be filled while setting
it to False will cause it to be non-filled.

Reference: [https://panel.holoviz.org/reference/indicators/BooleanStatus.html](https://panel.holoviz.org/reference/indicators/BooleanStatus.html)

Example:

\>\>\> BooleanStatus(value=True, color='primary', width=100, height=100)\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> margin, disabled
>
> `panel.widgets.indicators.Indicator`:
> sizing_mode
>
> href="panel.widgets.indicators.html#panel.widgets.indicators.BooleanIndicator"
> class="reference internal"
> title="panel.widgets.indicators.BooleanIndicator"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.indicators.BooleanIndicator:
> throttle
>
>

`value`` ``=`` ``Boolean(default=False,`` ``label='Value')`
Whether the indicator is active or not.

`height`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``default=20,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Height')`
height of the circle.

`width`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``default=20,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of the circle.

`color`` ``=`` ``Selector(default='dark',`` ``label='Color',`` ``names={},`` ``objects=['primary',`` ``'secondary',`` ``'success',`` ``'info',`` ``'danger',`` ``'warning',`` ``'light',`` ``'dark'])`
The color of the circle, one of ‘primary’, ‘secondary’, ‘success’,
‘info’, ‘danger’, ‘warning’, ‘light’, ‘dark’

class panel.ui.widgets.Breadcrumbs(\*, color, max_items, separator, active, items, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `BreadcrumbsBase`

The Breadcrumbs component is used to show the navigation path of a user
within an application. It improves usability by allowing users to track
their location and navigate back easily.

Breadcrumb items can be strings or objects with properties:

- label: The label of the breadcrumb item (required)

- icon: The icon of the breadcrumb item (optional)

- avatar: The avatar of the breadcrumb item (optional)

- href: Link to navigate to when clicking the breadcrumb item (optional)

- tooltip: The tooltip text shown on hover (optional)

References:

- [https://panel-material-ui.holoviz.org/reference/menus/Breadcrumbs.html](https://panel-material-ui.holoviz.org/reference/menus/Breadcrumbs.html)

- [https://mui.com/material-ui/react-breadcrumbs/](https://mui.com/material-ui/react-breadcrumbs/)

Example:

\>\>\> pmui.Breadcrumbs(items=\[\
...     {'label': 'Documentation', 'icon': 'article'},\
...     {'label': 'Reference Gallery', 'icon': 'category'},\
...     {'label': 'Menus', 'icon': 'menu'},\
...     {'label': 'Breadcrumbs', 'icon': 'grain'},\
... \], active=3)\

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
> label, attached, description, disabled
>
> `panel_material_ui.widgets.menus.MenuBase`:
> value, margin, width, active, items
>
> `panel_material_ui.widgets.menus.BreadcrumbsBase`:
> color, max_items, separator
>
>

class panel.ui.widgets.Button(\*, href, target, clicks, disable_elevation, end_icon, icon, icon_size, size, description_delay, attached, description, dark_theme, sx, theme_config, use_shadow_dom, button_style, button_type, color, variant, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_ButtonBase`,
`_ClickButton`

The Button widget allows triggering events when the button is clicked.

The Button provides a value parameter, which will toggle from False to
True while the click event is being processed.

It also provides an additional clicks parameter, that can be watched to
subscribe to click events.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/Button.html](https://panel-material-ui.holoviz.org/reference/widgets/Button.html)

- [https://panel.holoviz.org/reference/widgets/Button.html](https://panel.holoviz.org/reference/widgets/Button.html)

- [https://mui.com/material-ui/react-button/](https://mui.com/material-ui/react-button/)

Example:

\>\>\> Button(label='Click me', icon='caret-right', button_type='primary')\

Methods

|  |  |
|----|----|
| [on_click](#panel.ui.widgets.Button.on_click)(callback) | Register a callback to be executed when the Button is clicked. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
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
> label, margin, attached, disabled
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_style, button_type, color, description_delay
>
> `panel_material_ui.widgets.button._ButtonBase`:
> width, variant, clicks, disable_elevation, end_icon, icon, icon_size,
> size
>
>

`value`` ``=`` ``Event(default=False,`` ``label='Value')`
Toggles from False to True while the event is being processed.

`href`` ``=`` ``String(allow_None=True,`` ``label='Href')`
The URL to navigate to when the button is clicked.

`target`` ``=`` ``Selector(default='_self',`` ``label='Target',`` ``names={},`` ``objects=['_blank',`` ``'_parent',`` ``'_self',`` ``'_top'])`
Where to open the linked document.

on_click(callback: Callable\[\[Event\], None \| Awaitable\[None\]\]) → Watcher
Register a callback to be executed when the Button is clicked.

The callback is given an Event argument declaring the number of clicks

Returns:
watcher: param.Parameterized.Watcher
A Watcher that executes the callback when the button is clicked.

panel.ui.widgets.ButtonIcon
alias of
[IconButton](#panel.ui.widgets.IconButton)

class panel.ui.widgets.CheckBoxGroup(\*, color, inline, label_placement, size, attached, dark_theme, sx, theme_config, use_shadow_dom, description, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_RadioGroup`,
`MaterialMultiSelectBase`

The CheckBoxGroup widget allows selecting between a list of options by
ticking the corresponding checkboxes.

It falls into the broad category of multi-option selection widgets that
provide a compatible API that also include the CheckButtonGroup widget.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/CheckBoxGroup.html](https://panel-material-ui.holoviz.org/reference/widgets/CheckBoxGroup.html)

- [https://panel.holoviz.org/reference/widgets/CheckBoxGroup.html](https://panel.holoviz.org/reference/widgets/CheckBoxGroup.html)

- [https://mui.com/material-ui/react-checkbox/#formgroup](https://mui.com/material-ui/react-checkbox/#formgroup)

Example:

\>\>\> CheckBoxGroup(\
...     name='Fruits', value=\['Apple', 'Pear'\], options=\['Apple', 'Banana', 'Pear', 'Strawberry'\],\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
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
> `panel_material_ui.widgets.select._RadioGroup`:
> width, color, label_placement, size, inline
>
>

`value`` ``=`` ``List(allow_None=True,`` ``bounds=(0,`` ``None),`` ``label='Value')`
The selected values.

value = None

class panel.ui.widgets.CheckButtonGroup(\*, orientation, size, variant, button_style, button_type, color, description_delay, attached, dark_theme, sx, theme_config, use_shadow_dom, description, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_ButtonGroup`,
`MaterialMultiSelectBase`

The CheckButtonGroup widget allows selecting from a list or dictionary
of values using a set of toggle buttons.

It falls into the broad category of multi-option selection widgets that
provide a compatible API that also include the CheckBoxGroup widget.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/CheckButtonGroup.html](https://panel-material-ui.holoviz.org/reference/widgets/CheckButtonGroup.html)

- [https://panel.holoviz.org/reference/widgets/CheckButtonGroup.html](https://panel.holoviz.org/reference/widgets/CheckButtonGroup.html)

- [https://mui.com/material-ui/react-toggle-button/](https://mui.com/material-ui/react-toggle-button/)

Example:

\>\>\> CheckButtonGroup(\
...     label='Regression Models', value=\['Lasso', 'Ridge'\],\
...     options=\['Lasso', 'Linear', 'Ridge', 'Polynomial'\]\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
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
> label, margin, attached, disabled
>
> `panel_material_ui.widgets.select.MaterialMultiSelectBase`:
> value
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_style, button_type, color, description_delay
>
> `panel_material_ui.widgets.select._ButtonGroup`:
> width, orientation, size, variant
>
>

`active`` ``=`` ``List(bounds=(0,`` ``None),`` ``constant=True,`` ``default=[],`` ``item_type=<class`` ``'int'>,`` ``label='Active',`` ``readonly=True)`
Zero-based indices of the selected options in option order.

class panel.ui.widgets.Checkbox(\*, color, description_delay, indeterminate, size, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget)

The Checkbox allows toggling a single condition between True/False
states by ticking a checkbox.

This widget is interchangeable with the Switch widget.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/Checkbox.html](https://panel-material-ui.holoviz.org/reference/widgets/Checkbox.html)

- [https://panel.holoviz.org/reference/widgets/Checkbox.html](https://panel.holoviz.org/reference/widgets/Checkbox.html)

- [https://mui.com/material-ui/react-checkbox/](https://mui.com/material-ui/react-checkbox/)

Example:

\>\>\> Checkbox(label='Works with the tools you know and love', value=True)\

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

`value`` ``=`` ``Boolean(default=False,`` ``label='Value')`
The widget value which the widget type resolves to when used as a
reactive param reference.

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of the widget.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the checkbox.

`description_delay`` ``=`` ``Integer(default=1000,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Description`` ``delay')`
Delay (in milliseconds) to display the tooltip after the cursor has
hovered over the Button, default is 1000ms.

`indeterminate`` ``=`` ``Boolean(default=False,`` ``label='Indeterminate')`
Whether the checkbox can be in an indeterminate state. The indeterminate
state may only be set in Python.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The size of the checkbox.

width = None

class panel.ui.widgets.Chip(label=None, **params)
Bases: `_ButtonLike`,
`_ClickButton`

A Chip can be used to display information, labels, tags, or actions. It
can include text, an icon, or a delete button.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/Chip.html](https://panel-material-ui.holoviz.org/reference/widgets/Chip.html)

- [https://mui.com/material-ui/react-chip/](https://mui.com/material-ui/react-chip/)

Example:

\>\>\> Chip(label="Log Time", icon="clock")\

Methods

|  |  |
|----|----|
| [on_click](#panel.ui.widgets.Chip.on_click)(callback) | Register a callback to be executed when the Chip is clicked. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> value
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
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
> label, margin, attached
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_style, button_type, color, description_delay
>
>

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of the widget.

`disabled`` ``=`` ``Boolean(default=False,`` ``label='Disabled')`
Disables the Chip component, making it opaque and disabling click
events.

`clicks`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Clicks')`
Number of clicks.

`icon`` ``=`` ``String(allow_None=True,`` ``label='Icon')`
Name of the icon to display in the chip. Should be a valid Material UI
icon name (e.g., ‘favorite’, ‘delete’, ‘add’). The icon appears before
the chip label.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium'])`
Size of the chip component. Options: - ‘small’: Compact size for dense
layouts - ‘medium’: Standard size (default)

`variant`` ``=`` ``Selector(default='filled',`` ``label='Variant',`` ``names={},`` ``objects=['filled',`` ``'outlined'])`
Visual style variant of the chip. Options: - ‘filled’: Solid background
color (default) - ‘outlined’: Transparent background with colored border

`object`` ``=`` ``Parameter(allow_None=True,`` ``label='Object')`

on_click(callback: Callable\[\[Event\], None \| Awaitable\[None\]\]) → Watcher
Register a callback to be executed when the Chip is clicked.

Returns:
watcher: param.Parameterized.Watcher
A Watcher that executes the callback when the Chip is clicked.

width = None

class panel.ui.widgets.CircularProgress(\*, bgcolor, color, size, thickness, variant, with_label, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget)

The CircularProgress provides a visual representation as a spinner of
the loading status.

References:

- [https://panel-material-ui.holoviz.org/reference/indicators/CircularProgress.html](https://panel-material-ui.holoviz.org/reference/indicators/CircularProgress.html)

- [https://panel.holoviz.org/reference/indicators/CircularProgress.html](https://panel.holoviz.org/reference/indicators/CircularProgress.html)

- [https://mui.com/material-ui/react-progress/#circular](https://mui.com/material-ui/react-progress/#circular)

Example:

\>\>\> CircularProgress(color='success')\

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

`value`` ``=`` ``Number(bounds=(0,`` ``100),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
The value of the loading indicator.

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of the widget.

`bgcolor`` ``=`` ``Selector(label='Bgcolor',`` ``names={},`` ``objects=[None,`` ``'light',`` ``'dark'])`
The background color of the loading spinner.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the loading indicator.

`size`` ``=`` ``Integer(default=40,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Size')`
The size of the loading spinner.

`thickness`` ``=`` ``Number(default=3.6,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Thickness')`
The thickness of the loading spinner.

`variant`` ``=`` ``Selector(default='indeterminate',`` ``label='Variant',`` ``names={},`` ``objects=['determinate',`` ``'indeterminate'])`
The variant of the loading indicator.

`with_label`` ``=`` ``Boolean(default=False,`` ``label='With`` ``label')`
Whether to show a label indicating the progress.

width = None

class panel.ui.widgets.CodeEditor(\*, annotations, filename, indent, language, on_keyup, print_margin, readonly, soft_tabs, theme, value_input, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [Widget](panel.widgets.base.md#panel.widgets.base.Widget)

The CodeEditor widget allows displaying and editing code in the powerful
Ace editor.

Reference:
[https://panel.holoviz.org/reference/widgets/CodeEditor.html](https://panel.holoviz.org/reference/widgets/CodeEditor.html)

Example:

\>\>\> CodeEditor(value=py_code, language='python', theme='monokai')\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
>

`value`` ``=`` ``String(default='',`` ``label='Value')`
State of the current code in the editor if on_keyup. Otherwise, only
upon loss of focus, i.e. clicking outside the editor, or pressing
\<Ctrl+Enter\> or \<Cmd+Enter\>.

`annotations`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'dict'>,`` ``label='Annotations')`
List of annotations to add to the editor.

`filename`` ``=`` ``String(default='',`` ``label='Filename')`
Filename from which to deduce language

`language`` ``=`` ``String(default='text',`` ``label='Language')`
Language of the editor

`indent`` ``=`` ``Integer(default=4,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Indent')`
The default indent size.

`on_keyup`` ``=`` ``Boolean(default=True,`` ``label='On`` ``keyup')`
Whether to update the value on every key press or only upon loss of
focus / hotkeys.

`print_margin`` ``=`` ``Boolean(default=False,`` ``label='Print`` ``margin')`
Whether to show the a print margin.

`readonly`` ``=`` ``Boolean(default=False,`` ``label='Readonly')`
Define if editor content can be modified. Alias for disabled.

`soft_tabs`` ``=`` ``Boolean(default=False,`` ``label='Soft`` ``tabs')`
Whether to use spaces instead of tabs.

`theme`` ``=`` ``Selector(default='github_light_default',`` ``label='Theme',`` ``names={},`` ``objects=['ambiance',`` ``'chaos',`` ``'chrome',`` ``'cloud9_day',`` ``'cloud9_night',`` ``'clouds',`` ``'clouds_midnight',`` ``'cobalt',`` ``'crimson_editor',`` ``'dawn',`` ``'dracula',`` ``'dreamweaver',`` ``'eclipse',`` ``'github',`` ``'github_dark',`` ``'github_light_default',`` ``'gob',`` ``'gruvbox',`` ``'idle_fingers',`` ``'iplastic',`` ``'katzenmilch',`` ``'kr_theme',`` ``'kuroir',`` ``'merbivore',`` ``'merbivore_soft',`` ``'mono_industrial',`` ``'monokai',`` ``'nord_dark',`` ``'one_dark',`` ``'pastel_on_dark',`` ``'solarized_dark',`` ``'solarized_light',`` ``'sqlserver',`` ``'terminal',`` ``'textmate',`` ``'tomorrow',`` ``'tomorrow_night',`` ``'tomorrow_night_blue',`` ``'tomorrow_night_bright',`` ``'tomorrow_night_eighties',`` ``'twilight',`` ``'vibrant_ink',`` ``'xcode'])`
If no value is provided, it defaults to the current theme set by
pn.config.theme, as specified in the CodeEditor.THEME_CONFIGURATION
dictionary. If not defined there, it falls back to the default parameter
value.

`value_input`` ``=`` ``String(default='',`` ``label='Value`` ``input')`
State of the current code updated on every key press. Identical to value
if on_keyup.

class panel.ui.widgets.ColorMap(\*, error_state, helper_text, attached, description, dark_theme, sx, theme_config, use_shadow_dom, ncols, swatch_height, swatch_width, value_name, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget),
[ColorMap](panel.widgets.select.md#panel.widgets.select.ColorMap)

Select a colormap from a dictionary of palettes.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
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
> label, margin, width, attached, description, disabled
>
>

`value`` ``=`` ``Parameter(allow_None=True,`` ``label='Value')`
The selected colormap.

`options`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={},`` ``label='Options')`
Dictionary of colormaps.

`ncols`` ``=`` ``Integer(bounds=(1,`` ``None),`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Ncols')`
Number of columns of swatches to display.

`swatch_height`` ``=`` ``Integer(bounds=(1,`` ``None),`` ``default=20,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Swatch`` ``height')`
Height of the color swatches.

`swatch_width`` ``=`` ``Integer(bounds=(1,`` ``None),`` ``default=100,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Swatch`` ``width')`
Width of the color swatches.

`value_name`` ``=`` ``String(allow_None=True,`` ``label='Value`` ``name')`
Name of the selected colormap.

`error_state`` ``=`` ``Boolean(default=False,`` ``label='Error`` ``state')`
Whether to display the widget in an error state.

`helper_text`` ``=`` ``String(default='',`` ``label='Helper`` ``text')`
Helper text displayed below the widget.

class panel.ui.widgets.ColorPicker(\*, alpha, color, error_state, format, helper_text, size, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget)

The ColorPicker allows selecting a color value using a color picker
utility.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/ColorPicker.html](https://panel-material-ui.holoviz.org/reference/widgets/ColorPicker.html)

- [https://panel.holoviz.org/reference/widgets/ColorPicker.html](https://panel.holoviz.org/reference/widgets/ColorPicker.html)

- [https://viclafouch.github.io/mui-color-input/](https://viclafouch.github.io/mui-color-input/)

Example:

\>\>\> pmui.ColorPicker(name='Color Picker', value='#99ef78')\

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
> label, margin, width, attached, description, disabled
>
>

`value`` ``=`` ``String(allow_None=True,`` ``label='Value')`
The current color value.

`alpha`` ``=`` ``Boolean(default=False,`` ``label='Alpha')`
Whether to display input controls for a color’s alpha (transparency)
channel.

`error_state`` ``=`` ``Boolean(default=False,`` ``label='Error`` ``state')`
Whether to display in error state.

`helper_text`` ``=`` ``String(default='',`` ``label='Helper`` ``text')`
Helper text displayed below the color picker field.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The accent color of the color picker when active or focused.

`format`` ``=`` ``Selector(default='hex',`` ``label='Format',`` ``names={},`` ``objects=['hex',`` ``'rgb',`` ``'rgba',`` ``'hsl',`` ``'hsv'])`
The format of the color value. - hex: The hex color value. - rgb: The
rgb color value. - rgba: The rgba color value. - hsl: The hsl color
value. - hsv: The hsv color value.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The visual size of the input field

`variant`` ``=`` ``Selector(default='outlined',`` ``label='Variant',`` ``names={},`` ``objects=['filled',`` ``'outlined',`` ``'standard'])`
The visual style variant of the input field

class panel.ui.widgets.CompositeWidget(\*, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [Widget](panel.widgets.base.md#panel.widgets.base.Widget)

A baseclass for widgets which are made up of two or more other widgets

Methods

|  |  |
|----|----|
| [select](#panel.ui.widgets.CompositeWidget.select)(\[selector\]) | Iterates over the Viewable and any potential children in the applying the Selector. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label, value
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
>

select(selector: type \| Callable\[\[Viewable\], bool\] \| None = None) → list\[Viewable\]
Iterates over the Viewable and any potential children in the applying
the Selector.

Parameters:
**selector: type or callable or None**
The selector allows selecting a subset of Viewables by declaring a type
or callable function to filter by.

Returns:
viewables: list(Viewable)

class panel.ui.widgets.CrossSelector(\*, color, definition_order, filter_fn, searchable, size, visual_size, attached, dark_theme, sx, theme_config, use_shadow_dom, description, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MaterialMultiSelectBase`

The CrossSelector widget allows selecting multiple values from a list of
options.

It falls into the broad category of multi-value, option-selection
widgets that provide a compatible API and include the MultiSelect,
CrossSelector, CheckBoxGroup and CheckButtonGroup widgets.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/CrossSelector.html](https://panel-material-ui.holoviz.org/reference/widgets/CrossSelector.html)

- [https://panel.holoviz.org/reference/widgets/CrossSelector.html](https://panel.holoviz.org/reference/widgets/CrossSelector.html)

- [https://mui.com/material-ui/react-select/#multiple-select](https://mui.com/material-ui/react-select/#multiple-select)

Example:

\>\>\> CrossSelector(\
...     label='Favourites', value=\['Panel', 'hvPlot'\],\
...     options=\['Panel', 'hvPlot', 'HoloViews', 'GeoViews', 'Datashader', 'Param', 'Colorcet'\],\
...     max_items=2\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
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
> `panel_material_ui.widgets.select.MaterialMultiSelectBase`:
> value
>
>

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of the widget

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the cross selector widget.

`definition_order`` ``=`` ``Boolean(default=True,`` ``label='Definition`` ``order')`
Preserve option order when selecting values.

`filter_fn`` ``=`` ``Callable(label='Filter`` ``fn')`
Function receiving a query and an option label.

`searchable`` ``=`` ``Boolean(default=True,`` ``label='Searchable')`
Whether the dropdown is searchable

`size`` ``=`` ``Integer(default=10,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Size')`
The number of options shown at once (note this is the only way to
control the height of this widget)

`visual_size`` ``=`` ``Selector(default='medium',`` ``label='Visual`` ``size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The visual size of the cross selector.

filter_fn(string, flags=0)
Scan through string looking for a match to the pattern, returning a
Match object, or None if no match was found.

width = None

class panel.ui.widgets.DatePicker(\*, as_numpy_datetime64, clearable, disable_future, disable_past, disabled_dates, enabled_dates, end, format, open_to, size, start, views, color, error_state, helper_text, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_DatePickerBase`

The DatePicker allows selecting a date value using a text box and a
date-picking utility.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/DatePicker.html](https://panel-material-ui.holoviz.org/reference/widgets/DatePicker.html)

- [https://panel.holoviz.org/reference/widgets/DatePicker.html](https://panel.holoviz.org/reference/widgets/DatePicker.html)

- [https://mui.com/x/react-date-pickers/date-picker/](https://mui.com/x/react-date-pickers/date-picker/)

Example:

\>\>\> DatePicker(\
...     value=date(2025,1,1),\
...     start=date(2025,1,1), end=date(2025,12,31),\
...     name='Date'\
... )\

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
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._DatePickerBase`:
> width, size, as_numpy_datetime64, clearable, disabled_dates,
> disable_future, disable_past, enabled_dates, end, format, open_to,
> start, views
>
>

`value`` ``=`` ``Date(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
The current value. Can be a datetime object or a string in ISO format.

class panel.ui.widgets.DateRangePicker(\*, disabled_dates, enabled_dates, end, format, size, start, color, error_state, helper_text, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MaterialInputWidget`

The DateRangePicker allows selecting a date range using a calendar-based
picker with two months displayed side by side.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/DateRangePicker.html](https://panel-material-ui.holoviz.org/reference/widgets/DateRangePicker.html)

- [https://daypicker.dev/](https://daypicker.dev/)

Example:

\>\>\> DateRangePicker(\
...     value=(date(2025,1,9), date(2025,1,16)),\
...     start=date(2025,1,1), end=date(2025,12,31),\
...     name='Date Range'\
... )\

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
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
>

`value`` ``=`` ``DateRange(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value',`` ``length=2)`
The selected date range as a tuple of two dates.

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``default=300,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of this component. If sizing_mode is set to stretch or scale mode
this will merely be used as a suggestion.

`disabled_dates`` ``=`` ``DateList(bounds=(0,`` ``None),`` ``default=[],`` ``label='Disabled`` ``dates')`
Dates to make unavailable for selection.

`enabled_dates`` ``=`` ``DateList(bounds=(0,`` ``None),`` ``default=[],`` ``label='Enabled`` ``dates')`
Dates to make available for selection.

`end`` ``=`` ``Date(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End')`
The maximum selectable date.

`format`` ``=`` ``String(default='YYYY-MM-DD',`` ``label='Format')`
Format of the date when rendered in the input.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The visual size of the date range picker input.

`start`` ``=`` ``Date(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Start')`
The minimum selectable date.

`value_start`` ``=`` ``Date(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``start',`` ``readonly=True)`
The lower value of the selected range.

`value_end`` ``=`` ``Date(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``end',`` ``readonly=True)`
The upper value of the selected range.

class panel.ui.widgets.DateRangeSlider(\*, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_RangeSliderBase`

The DateRangeSlider widget allows selecting a date range using a slider
with two handles. Supports datetime.datetime, datetime.date and
np.datetime64 ranges.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/DateRangeSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/DateRangeSlider.html)

- [https://panel.holoviz.org/reference/widgets/DateRangeSlider.html](https://panel.holoviz.org/reference/widgets/DateRangeSlider.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

Example:

\>\>\> import datetime as dt\
\>\>\> DateRangeSlider(\
...     value=(dt.datetime(2025, 1, 9), dt.datetime(2025, 1, 16)),\
...     start=dt.datetime(2025, 1, 1),\
...     end=dt.datetime(2025, 1, 31),\
...     step=2,\
...     name="A tuple of datetimes"\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> bar_color, direction, tooltips, color, marks, size, track,
> value_label, inline_layout
>
>

`value`` ``=`` ``DateRange(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value',`` ``length=2,`` ``nested_refs=True)`
The selected range as a tuple of values. Updated when one of the handles
is dragged. Supports datetime.datetime, datetime.date, and np.datetime64
ranges.

`start`` ``=`` ``Date(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Start')`
The lower bound.

`end`` ``=`` ``Date(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End')`
The upper bound.

`format`` ``=`` ``String(allow_None=True,`` ``label='Format')`
Datetime format used for parsing and formatting the date.

`step`` ``=`` ``Number(default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Step')`
The step size in days. Default is 1 day.

`value_throttled`` ``=`` ``DateRange(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``throttled',`` ``length=2,`` ``nested_refs=True)`
The selected range as a tuple of values. Updated one of the handles is
released. Supports datetime.datetime, datetime.date and np.datetime64
ranges

`value_start`` ``=`` ``Date(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``start',`` ``readonly=True)`
The lower value of the selected range.

`value_end`` ``=`` ``Date(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``end',`` ``readonly=True)`
The upper value of the selected range.

end = None

format = None

start = None

value = None

value_throttled = None

class panel.ui.widgets.DateSlider(\*, as_datetime, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_ContinuousSlider`

The DateSlider widget allows selecting a value within a set of bounds
using a slider. Supports datetime.datetime, datetime.date and
np.datetime64 values. The step size is fixed at 1 day.

References:

- [https://panel.holoviz.org/reference/widgets/DateSlider.html](https://panel.holoviz.org/reference/widgets/DateSlider.html)

Example:

\>\>\> import datetime as dt\
\>\>\> DateSlider(\
...     value=dt.datetime(2025, 1, 1),\
...     start=dt.datetime(2025, 1, 1),\
...     end=dt.datetime(2025, 1, 7),\
...     name="A datetime value"\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> bar_color, direction, tooltips, color, marks, size, track,
> value_label, inline_layout
>
>

`value`` ``=`` ``Date(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
The selected date value of the slider. Updated when the slider handle is
dragged. Supports datetime.datetime, datetime.date or np.datetime64
types.

`start`` ``=`` ``Date(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Start')`
The lower bound.

`end`` ``=`` ``Date(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End')`
The upper bound.

`format`` ``=`` ``String(allow_None=True,`` ``label='Format')`
Datetime format used for parsing and formatting the date.

`step`` ``=`` ``Integer(bounds=(1,`` ``None),`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Step')`
The step parameter in days.

`value_throttled`` ``=`` ``Date(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``throttled')`
The value of the slider. Updated when the slider handle is released.

`as_datetime`` ``=`` ``Boolean(default=False,`` ``label='As`` ``datetime')`
Whether to store the date as a datetime.

end = None

format = None

start = None

value = None

class panel.ui.widgets.DatetimeInput(\*, enter_pressed, max_length, size, color, error_state, helper_text, variant, attached, dark_theme, sx, theme_config, use_shadow_dom, end, format, start, description, placeholder, serializer, type, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [TextInput](#panel.ui.widgets.TextInput),
[DatetimeInput](panel.widgets.input.md#panel.widgets.input.DatetimeInput)

The DatetimeInput allows entering a datetime value using a text input
box.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal"
> title="panel.widgets.input.LiteralInput"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets. input .LiteralInput](panel.widgets.input.md#panel.widgets.input.LiteralInput):
> serializer, type
>
> [class="reference internal"
> title="panel.widgets.input.DatetimeInput"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets. input .DatetimeInput](panel.widgets.input.md#panel.widgets.input.DatetimeInput):
> start, end, format
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._TextInputBase`:
> max_length, placeholder, size
>
> [title="panel_material_ui.widgets.input.TextInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets. input .TextInput](#panel.ui.widgets.TextInput):
> enter_pressed
>
>

`value`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'datetime.datetime'>,`` ``<class`` ``'datetime.date'>,`` ``<class`` ``'str'>),`` ``label='Value')`
The current value. Can be a datetime object or a string in ISO format.

`value_input`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'datetime.datetime'>,`` ``<class`` ``'datetime.date'>,`` ``<class`` ``'str'>),`` ``constant=True,`` ``label='Value`` ``input',`` ``readonly=True)`
The current value. Can be a datetime object or a string in ISO format.

value = None

value_input = None

class panel.ui.widgets.DatetimePicker(\*, enable_seconds, enable_time, military_time, as_numpy_datetime64, clearable, disable_future, disable_past, disabled_dates, enabled_dates, end, format, open_to, size, start, views, color, error_state, helper_text, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_DatetimePickerBase`

The DatetimePicker allows selecting selecting a datetime value using a
textbox and a datetime-picking utility.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/DatetimePicker.html](https://panel-material-ui.holoviz.org/reference/widgets/DatetimePicker.html)

- [https://panel.holoviz.org/reference/widgets/DatetimePicker.html](https://panel.holoviz.org/reference/widgets/DatetimePicker.html)

- [https://mui.com/x/react-date-pickers/date-time-picker/](https://mui.com/x/react-date-pickers/date-time-picker/)

Example:

\>\>\> DatetimePicker(\
...    value=datetime(2025,1,1,22,0),\
...    start=date(2025,1,1), end=date(2025,12,31),\
...    military_time=True, name='Date and time'\
... )\

Also supports string values:

\>\>\> DatetimePicker(\
...    value="2025-01-01 22:00:00",\
...    military_time=True, name='Date and time'\
... )\

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
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._DatePickerBase`:
> width, size, as_numpy_datetime64, clearable, disabled_dates,
> disable_future, disable_past, enabled_dates
>
> `panel_material_ui.widgets.input._DatetimePickerBase`:
> format, open_to, views, enable_seconds, enable_time, military_time
>
>

`value`` ``=`` ``Datetime(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
The current value. Can be a datetime object or a string in ISO format.

`end`` ``=`` ``Datetime(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End')`
The maximum selectable datetime.

`start`` ``=`` ``Datetime(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Start')`
The minimum selectable datetime.

class panel.ui.widgets.DatetimeRangeInput(\*, end, format, start, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [DatetimeRangeInput](panel.widgets.input.md#panel.widgets.input.DatetimeRangeInput)

A datetime range composed of two Material datetime inputs.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
> href="panel.widgets.input.html#panel.widgets.input.DatetimeRangeInput"
> class="reference internal"
> title="panel.widgets.input.DatetimeRangeInput"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets. input .DatetimeRangeInput:
> value, start, end, format
>
>

class panel.ui.widgets.DatetimeRangePicker(\*, enable_seconds, military_time, disabled_dates, enabled_dates, end, format, size, start, color, error_state, helper_text, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases:
[DateRangePicker](#panel.ui.widgets.DateRangePicker)

The DatetimeRangePicker allows selecting a datetime range using a
calendar-based picker with two months displayed side by side and time
inputs for start and end times.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/DatetimeRangePicker.html](https://panel-material-ui.holoviz.org/reference/widgets/DatetimeRangePicker.html)

- [https://daypicker.dev/](https://daypicker.dev/)

Example:

\>\>\> DatetimeRangePicker(\
...     value=(datetime(2025,1,9,8,0), datetime(2025,1,16,17,0)),\
...     start=datetime(2025,1,1), end=datetime(2025,12,31),\
...     name='Datetime Range'\
... )\

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
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> [title="panel_material_ui.widgets.input.DateRangePicker"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets. input .DateRangePicker](#panel.ui.widgets.DateRangePicker):
> width, disabled_dates, enabled_dates, size
>
>

`value`` ``=`` ``DateRange(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value',`` ``length=2)`
The selected datetime range as a tuple of two datetimes.

`end`` ``=`` ``Datetime(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End')`
The maximum selectable datetime.

`format`` ``=`` ``String(allow_None=True,`` ``label='Format')`
Format of the datetime when rendered in the input. If None, will be set
automatically based on military_time setting.

`start`` ``=`` ``Datetime(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Start')`
The minimum selectable datetime.

`value_start`` ``=`` ``Date(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``start',`` ``readonly=True)`
The lower value of the selected range.

`value_end`` ``=`` ``Date(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``end',`` ``readonly=True)`
The upper value of the selected range.

`enable_seconds`` ``=`` ``Boolean(default=True,`` ``label='Enable`` ``seconds')`
Enable editing of seconds in the time inputs.

`military_time`` ``=`` ``Boolean(default=True,`` ``label='Military`` ``time')`
Whether to display time in 24 hour format.

format = None

class panel.ui.widgets.DatetimeRangeSlider(\*, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases:
[DateRangeSlider](#panel.ui.widgets.DateRangeSlider)

The DatetimeRangeSlider widget allows selecting a datetime range using a
slider with two handles. Supports datetime.datetime and np.datetime64
ranges.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/DatetimeRangeSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/DatetimeRangeSlider.html)

- [https://panel.holoviz.org/reference/widgets/DatetimeRangeSlider.html](https://panel.holoviz.org/reference/widgets/DatetimeRangeSlider.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

Example:

\>\>\> import datetime as dt\
\>\>\> DatetimeRangeSlider(\
...     value=(dt.datetime(2025, 1, 9), dt.datetime(2025, 1, 16)),\
...     start=dt.datetime(2025, 1, 1),\
...     end=dt.datetime(2025, 1, 31),\
...     step=60\*60,\
...     label="A tuple of datetimes"\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> bar_color, direction, tooltips, color, marks, size, track,
> value_label, inline_layout
>
> [title="panel_material_ui.widgets.slider.DateRangeSlider"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets.slider.DateRangeSlider](#panel.ui.widgets.DateRangeSlider):
> value, start, end, format, value_throttled, value_start, value_end
>
>

`step`` ``=`` ``Number(default=60,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Step')`
The step size in seconds. Default is 1 minute, i.e 60 seconds.

class panel.ui.widgets.DatetimeSlider(\*, as_datetime, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [DateSlider](#panel.ui.widgets.DateSlider)

The DatetimeSlider widget allows selecting a value within a set of
bounds using a slider. Supports datetime.date, datetime.datetime and
np.datetime64 values. The step size is fixed at 1 minute.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/DatetimeSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/DatetimeSlider.html)

- [https://panel.holoviz.org/reference/widgets/DatetimeSlider.html](https://panel.holoviz.org/reference/widgets/DatetimeSlider.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

Example:

\>\>\> import datetime as dt\
\>\>\> DatetimeSlider(\
...     value=dt.datetime(2025, 1, 1),\
...     start=dt.datetime(2025, 1, 1),\
...     end=dt.datetime(2025, 1, 7),\
...     name="A datetime value"\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> bar_color, direction, tooltips, color, marks, size, track,
> value_label, inline_layout
>
> [title="panel_material_ui.widgets.slider.DateSlider"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets.slider.DateSlider](#panel.ui.widgets.DateSlider):
> value, start, end, format, value_throttled
>
>

`step`` ``=`` ``Number(bounds=(1,`` ``None),`` ``default=60,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Step')`
The step size in seconds. Default is 1 minute, i.e 60 seconds.

`as_datetime`` ``=`` ``Boolean(constant=True,`` ``default=True,`` ``label='As`` ``datetime',`` ``readonly=True)`
Whether to store the date as a datetime.

class panel.ui.widgets.Debugger(\*, \_number_of_errors, \_number_of_infos, \_number_of_warnings, formatter_args, level, logger_names, only_last, collapsed, collapsible, header, header_background, header_color, header_css_classes, hide_header, outlined, title, title_css_classes, title_variant, \_headers, \_names, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, objects, elevation, raised, square, variant, name)
Bases: [Card](panel.ui.layout.md#panel.ui.layout.Card)

An uneditable Card holding a terminal that prints the logs of your
callbacks. By default only exceptions are printed; to add your own logs
use the panel.callbacks logger in your callbacks: logger =
logging.getLogger(‘panel.callbacks’)

Example:

\>\>\> Debugger(title='Debugger', level=logging.INFO)\

Methods

|                        |     |
|------------------------|-----|
| **acknowledge_errors** |     |
| **update_log_counts**  |     |

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
> [class="reference internal"
> title="panel_material_ui.layout.base.Card"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.Card](panel.ui.layout.md#panel.ui.layout.Card):
> collapsible, header, header_background, header_color,
> header_css_classes, hide_header, outlined, title_css_classes,
> title_variant
>
>

`collapsed`` ``=`` ``Boolean(default=True,`` ``label='Collapsed')`
Whether the contents of the Card are collapsed.

`title`` ``=`` ``String(default='Debugger',`` ``label='Title')`
The title displayed in the header of the Debugger.

`_number_of_errors`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='`` ``number`` ``of`` ``errors')`
Number of logged errors since last acknowledged.

`_number_of_warnings`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='`` ``number`` ``of`` ``warnings')`
Number of logged warnings since last acknowledged.

`_number_of_infos`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='`` ``number`` ``of`` ``infos')`
Number of logged information since last acknowledged.

`formatter_args`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={'fmt':`` ``'%(asctime)s`` ``[%(name)s`` ``-`` ``%(levelname)s]:`` ``%(message)s'},`` ``label='Formatter`` ``args')`
Arguments to pass to the logging formatter. See the standard python
logging libraries.

`level`` ``=`` ``Integer(default=40,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Level')`
Logging level to print in the debugger terminal.

`logger_names`` ``=`` ``List(bounds=(1,`` ``None),`` ``default=['panel'],`` ``item_type=<class`` ``'str'>,`` ``label='Logger`` ``names')`
Loggers which will be prompted in the debugger terminal.

`only_last`` ``=`` ``Boolean(default=True,`` ``label='Only`` ``last')`
Whether only the last stack is printed or the full.

class panel.ui.widgets.Dial(\*, annulus_width, background, bounds, colors, default_color, end_angle, format, label_color, nan_format, needle_color, needle_width, start_angle, tick_size, title_size, unfilled_color, value_size, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [ValueIndicator](panel.widgets.indicators.md#panel.widgets.indicators.ValueIndicator)

A Dial represents a value in some range as a position on an annular
dial. It is similar to a Gauge but more minimal visually.

Reference:
[https://panel.holoviz.org/reference/indicators/Dial.html](https://panel.holoviz.org/reference/indicators/Dial.html)

Example:

\>\>\> Dial(label='Speed', value=79, format="{value} km/h", bounds=(0, 200), colors=\[(0.4, 'green'), (1, 'red')\])\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> margin, disabled
>
> `panel.widgets.indicators.Indicator`:
> sizing_mode
>
>

`value`` ``=`` ``Number(allow_None=True,`` ``default=25,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
Value to indicate on the dial a value within the declared bounds.

`height`` ``=`` ``Integer(allow_None=True,`` ``bounds=(1,`` ``None),`` ``default=250,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Height')`
The height of the component (in pixels). This can be either fixed or
preferred height, depending on height sizing policy.

`width`` ``=`` ``Integer(allow_None=True,`` ``bounds=(1,`` ``None),`` ``default=250,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
The width of the component (in pixels). This can be either fixed or
preferred width, depending on width sizing policy.

`annulus_width`` ``=`` ``Number(default=0.2,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Annulus`` ``width')`
Width of the radial annulus as a fraction of the total.

`background`` ``=`` ``Parameter(allow_None=True,`` ``label='Background')`
Background color of the component.

`bounds`` ``=`` ``Range(default=(0,`` ``100),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Bounds',`` ``length=2)`
The upper and lower bound of the dial.

`colors`` ``=`` ``List(allow_None=True,`` ``bounds=(0,`` ``None),`` ``item_type=<class`` ``'tuple'>,`` ``label='Colors')`
Color thresholds for the Dial, specified as a list of tuples of the
fractional threshold and the color to switch to.

`default_color`` ``=`` ``String(default='lightblue',`` ``label='Default`` ``color')`
Color of the radial annulus if not color thresholds are supplied.

`end_angle`` ``=`` ``Number(default=25,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End`` ``angle')`
Angle at which the dial ends.

`format`` ``=`` ``String(default='{value}%',`` ``label='Format')`
Formatting string for the value indicator and lower/upper bounds.

`label_color`` ``=`` ``String(allow_None=True,`` ``label='Label`` ``color')`
Color for all extraneous labels. Defaults to black, or white in the dark
theme.

`nan_format`` ``=`` ``String(default='-',`` ``label='Nan`` ``format')`
How to format nan values.

`needle_color`` ``=`` ``String(allow_None=True,`` ``label='Needle`` ``color')`
Color of the Dial needle. Defaults to black, or white in the dark theme.

`needle_width`` ``=`` ``Number(default=0.1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Needle`` ``width')`
Radial width of the needle.

`start_angle`` ``=`` ``Number(default=-205,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Start`` ``angle')`
Angle at which the dial starts.

`tick_size`` ``=`` ``String(allow_None=True,`` ``label='Tick`` ``size')`
Font size of the Dial min/max labels.

`title_size`` ``=`` ``String(allow_None=True,`` ``label='Title`` ``size')`
Font size of the Dial title.

`unfilled_color`` ``=`` ``String(allow_None=True,`` ``label='Unfilled`` ``color')`
Color of the unfilled region of the Dial. Defaults to a light or dark
grey depending on the theme.

`value_size`` ``=`` ``String(allow_None=True,`` ``label='Value`` ``size')`
Font size of the Dial value label.

class panel.ui.widgets.DictInput(\*, enter_pressed, max_length, size, color, error_state, helper_text, variant, attached, dark_theme, sx, theme_config, use_shadow_dom, description, placeholder, serializer, type, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases:
[LiteralInput](#panel.ui.widgets.LiteralInput)

The DictInput allows entering a dictionary value using a text input box.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal"
> title="panel.widgets.input.LiteralInput"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets. input .LiteralInput](panel.widgets.input.md#panel.widgets.input.LiteralInput):
> serializer
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._TextInputBase`:
> max_length, placeholder, size
>
> [title="panel_material_ui.widgets.input.TextInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets. input .TextInput](#panel.ui.widgets.TextInput):
> enter_pressed
>
> [title="panel_material_ui.widgets.input.LiteralInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets. input .LiteralInput](#panel.ui.widgets.LiteralInput):
> value_input
>
>

`value`` ``=`` ``Parameter(default={},`` ``label='Value')`
The widget value which the widget type resolves to when used as a
reactive param reference.

`type`` ``=`` ``ClassSelector(class_=<class`` ``'type'>,`` ``constant=True,`` ``default=<class`` ``'dict'>,`` ``label='Type',`` ``readonly=True)`
The type of the value.

type
alias of `dict`

class panel.ui.widgets.DiscretePlayer(\*, color, size, variant, attached, description, dark_theme, sx, theme_config, use_shadow_dom, value_throttled, direction, interval, loop_policy, preview_duration, scale_buttons, show_loop_controls, show_value, step, value_align, visible_buttons, visible_loop_options, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_PlayerBase`,
[DiscretePlayer](panel.widgets.player.md#panel.widgets.player.DiscretePlayer)

The DiscretePlayer provides controls to iterate through a list of
discrete options. The speed at which the widget plays is defined by the
interval (in milliseconds), but it is also possible to skip items using
the step parameter.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/DiscretePlayer.html](https://panel-material-ui.holoviz.org/reference/widgets/DiscretePlayer.html)

- [https://panel.holoviz.org/reference/widgets/DiscretePlayer.html](https://panel.holoviz.org/reference/widgets/DiscretePlayer.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

Example:

\>\>\> DiscretePlayer(\
...     label='Discrete Player',\
...     options=\[2, 4, 8, 16, 32, 64, 128\], value=32,\
...     loop_policy='loop'\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.player.PlayerBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.player.PlayerBase](panel.widgets.player.md#panel.widgets.player.PlayerBase):
> direction, loop_policy, preview_duration, show_loop_controls, step,
> value_align, scale_buttons, visible_buttons, visible_loop_options
>
> [class="reference internal"
> title="panel.widgets.player.DiscretePlayer"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.player.DiscretePlayer](panel.widgets.player.md#panel.widgets.player.DiscretePlayer):
> value, interval, show_value, value_throttled
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
> `panel_material_ui.widgets.player._PlayerBase`:
> height, width, color, size, variant
>
>

`options`` ``=`` ``ClassSelector(class_=(<class`` ``'dict'>,`` ``<class`` ``'list'>),`` ``default=[],`` ``label='Options')`
A list or dictionary of valid options.

class panel.ui.widgets.DiscreteSlider(\*, formatter, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [IntSlider](#panel.ui.widgets.IntSlider),
[SingleSelectBase](panel.widgets.select.md#panel.widgets.select.SingleSelectBase)

The DiscreteSlider widget allows selecting a discrete value using a
slider.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/DiscreteSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/DiscreteSlider.html)

- [https://panel.holoviz.org/reference/widgets/DiscreteSlider.html](https://panel.holoviz.org/reference/widgets/DiscreteSlider.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> bar_color, direction, tooltips, color, marks, size, track,
> value_label, inline_layout
>
> [title="panel_material_ui.widgets.slider.IntSlider"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets.slider.IntSlider](#panel.ui.widgets.IntSlider):
> format
>
>

`value`` ``=`` ``Parameter(allow_None=True,`` ``default=0,`` ``label='Value')`
The selected value of the slider. Updated when the handle is dragged.
Must be one of the options.

`options`` ``=`` ``ClassSelector(class_=(<class`` ``'dict'>,`` ``<class`` ``'list'>),`` ``default=[],`` ``label='Options')`
A list or dictionary of valid options.

`start`` ``=`` ``Integer(constant=True,`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Start',`` ``readonly=True)`
The starting value of the slider.

`end`` ``=`` ``Integer(constant=True,`` ``default=100,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End',`` ``readonly=True)`
The ending value of the slider.

`step`` ``=`` ``Integer(bounds=(1,`` ``None),`` ``constant=True,`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Step',`` ``readonly=True)`
The step size for the slider.

`value_throttled`` ``=`` ``Parameter(allow_None=True,`` ``constant=True,`` ``default=0,`` ``label='Value`` ``throttled')`
The value of the slider. Updated when the handle is released.

`formatter`` ``=`` ``String(default='%.3g',`` ``label='Formatter')`
Format applied to numeric option labels.

class panel.ui.widgets.EditableFloatSlider(\*, fixed_end, fixed_start, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_EditableContinuousSliderBase`,
[FloatSlider](#panel.ui.widgets.FloatSlider)

The EditableFloatSlider widget allows selecting a numeric floating-point
value within a set of bounds using a slider and for more precise control
offers an editable number input box.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/EditableFloatSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/EditableFloatSlider.html)

- [https://panel.holoviz.org/reference/widgets/EditableFloatSlider.html](https://panel.holoviz.org/reference/widgets/EditableFloatSlider.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

Example:

\>\>\> EditableFloatSlider(\
...     value=1.0, start=0.0, end=2.0, step=0.25, label="A float value"\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> value, bar_color, direction, tooltips, color, start, end, format,
> marks, size, track, value_label, value_throttled, inline_layout
>
> [title="panel_material_ui.widgets.slider.FloatSlider"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets.slider.FloatSlider](#panel.ui.widgets.FloatSlider):
> step
>
>

`fixed_start`` ``=`` ``Number(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Fixed`` ``start')`
A fixed lower bound for the slider and input.

`fixed_end`` ``=`` ``Number(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Fixed`` ``end')`
A fixed upper bound for the slider and input.

class panel.ui.widgets.EditableIntRangeSlider(\*, fixed_end, fixed_start, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_EditableRangeSliderBase`,
[IntRangeSlider](#panel.ui.widgets.IntRangeSlider)

The EditableIntRangeSlider widget allows selecting an integer range
using a slider with two handles and for more precise control offers an
editable integer input box.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/EditableIntRangeSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/EditableIntRangeSlider.html)

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> bar_color, direction, tooltips, color, marks, size, track,
> value_label, inline_layout
>
> `panel_material_ui.widgets.slider._RangeSliderBase`:
> value_throttled
>
> [title="panel_material_ui.widgets.slider.IntRangeSlider"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets.slider.IntRangeSlider](#panel.ui.widgets.IntRangeSlider):
> start, end, format, step, value_start, value_end
>
> `panel_material_ui.widgets.slider._EditableRangeSliderBase`:
> value
>
>

`fixed_start`` ``=`` ``Integer(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Fixed`` ``start')`
A fixed lower bound for the slider and input.

`fixed_end`` ``=`` ``Integer(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Fixed`` ``end')`
A fixed upper bound for the slider and input.

class panel.ui.widgets.EditableIntSlider(\*, fixed_end, fixed_start, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_EditableContinuousSliderBase`,
[IntSlider](#panel.ui.widgets.IntSlider)

The EditableIntSlider widget allows selecting an integer value within a
set of bounds using a slider and for more precise control offers an
editable integer input box.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/EditableIntSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/EditableIntSlider.html)

- [https://panel.holoviz.org/reference/widgets/EditableIntSlider.html](https://panel.holoviz.org/reference/widgets/EditableIntSlider.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

Example:

\>\>\> EditableIntSlider(\
...     value=2, start=0, end=5, step=1, label="An integer value"\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> bar_color, direction, tooltips, color, marks, size, track,
> value_label, inline_layout
>
> [title="panel_material_ui.widgets.slider.IntSlider"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets.slider.IntSlider](#panel.ui.widgets.IntSlider):
> value, start, end, format, step, value_throttled
>
>

`fixed_start`` ``=`` ``Integer(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Fixed`` ``start')`
A fixed lower bound for the slider and input.

`fixed_end`` ``=`` ``Integer(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Fixed`` ``end')`
A fixed upper bound for the slider and input.

class panel.ui.widgets.EditableRangeSlider(\*, fixed_end, fixed_start, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_EditableRangeSliderBase`,
[RangeSlider](#panel.ui.widgets.RangeSlider)

The EditableRangeSlider widget allows selecting a floating-point range
using a slider with two handles and for more precise control offers an
editable number input box.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/EditableFloatRangeSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/EditableFloatRangeSlider.html)

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> bar_color, direction, tooltips, color, start, end, format, marks,
> size, track, value_label, inline_layout
>
> `panel_material_ui.widgets.slider._RangeSliderBase`:
> value_throttled, value_start, value_end
>
> [title="panel_material_ui.widgets.slider.RangeSlider"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets.slider.RangeSlider](#panel.ui.widgets.RangeSlider):
> step
>
> `panel_material_ui.widgets.slider._EditableRangeSliderBase`:
> value
>
>

`fixed_start`` ``=`` ``Number(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Fixed`` ``start')`
A fixed lower bound for the slider and input.

`fixed_end`` ``=`` ``Number(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Fixed`` ``end')`
A fixed upper bound for the slider and input.

class panel.ui.widgets.Fab(\*, href, target, clicks, disable_elevation, end_icon, icon, icon_size, size, description_delay, attached, description, dark_theme, sx, theme_config, use_shadow_dom, button_style, button_type, color, variant, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [Button](#panel.ui.widgets.Button)

The Fab is a floating action button that allows triggering events when
the button is clicked.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/Fab.html](https://panel-material-ui.holoviz.org/reference/widgets/Fab.html)

- [https://mui.com/material-ui/react-floating-action-button/](https://mui.com/material-ui/react-floating-action-button/)

Example:

\>\>\> Fab(icon='add')\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
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
> label, margin, attached, disabled
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_type, color, description_delay
>
> `panel_material_ui.widgets.button._ButtonBase`:
> width, clicks, disable_elevation, end_icon
>
> [title="panel_material_ui.widgets.button.Button"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets.button.Button](#panel.ui.widgets.Button):
> value, href, target
>
>

`button_style`` ``=`` ``Selector(label='Button`` ``style',`` ``names={},`` ``objects=['circular',`` ``'extended'])`
The variant of the component (alias for variant to match Panel’s Button
API).

`variant`` ``=`` ``Selector(default='circular',`` ``label='Variant',`` ``names={},`` ``objects=['circular',`` ``'extended'])`
The variant of the button.

`icon`` ``=`` ``String(allow_None=True,`` ``default='add',`` ``label='Icon')`
The icon to display on the button.

`icon_size`` ``=`` ``String(default='1.5em',`` ``label='Icon`` ``size')`
Size of the icon as a string, e.g. 12px or 1em.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The size of the button.

button_style: t.Literal\['circular', 'extended'\] \| None = None

class panel.ui.widgets.FileDownload(file=None, **params)
Bases: `_ButtonBase`,
[FileDownload](panel.widgets.misc.md#panel.widgets.misc.FileDownload)

The FileDownload widget allows a user to download a file.

It works either by sending the file data to the browser on
initialization ([\`](#id1)embed\`=True), or when the button is
clicked.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/FileDownload.html](https://panel-material-ui.holoviz.org/reference/widgets/FileDownload.html)

- [https://panel.holoviz.org/reference/widgets/FileDownload.html](https://panel.holoviz.org/reference/widgets/FileDownload.html)

- [https://mui.com/material-ui/react-button/](https://mui.com/material-ui/react-button/)

Example:

\>\>\> FileDownload(file='IntroductionToPanel.ipynb', filename='intro.ipynb')\

Methods

|  |  |
|----|----|
| [transfer](#panel.ui.widgets.FileDownload.transfer)(\[download\]) | Transfers current data to the frontend. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> value
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.misc.FileDownload"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.misc.FileDownload](panel.widgets.misc.md#panel.widgets.misc.FileDownload):
> auto, callback, data, embed, file, filename, \_clicks, \_transfers
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
> label, margin, attached, disabled
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_style, button_type, color, description_delay
>
> `panel_material_ui.widgets.button._ButtonBase`:
> width, variant, clicks, disable_elevation, end_icon, icon, size
>
>

`icon_size`` ``=`` ``String(default='1em',`` ``label='Icon`` ``size')`
Size of the icon as a string, e.g. 12px or 1em.

`_syncing`` ``=`` ``Boolean(default=False,`` ``label='`` ``syncing')`
If auto is False track syncing data state.

transfer(download: bool = False)
Transfers current data to the frontend.

Parameters:
**download: bool**
If True, the data will automatically be downloaded once the data is
transferred.

class panel.ui.widgets.FileDropper(\*, accepted_filetypes, chunk_size, layout, max_file_size, max_files, max_total_file_size, mime_type, multiple, previews, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [Widget](panel.widgets.base.md#panel.widgets.base.Widget)

The FileDropper allows the user to upload one or more files to the
server.

It is similar to the FileInput widget but additionally adds support for
chunked uploads, making it possible to upload large files. The UI also
supports previews for image files. Unlike FileInput the uploaded files
are stored as dictionary of bytes object indexed by the filename.

Reference:
[https://panel.holoviz.org/reference/widgets/FileDropper.html](https://panel.holoviz.org/reference/widgets/FileDropper.html)

Example:

\>\>\> FileDropper(accepted_filetypes=\['image/\*'\], multiple=True)\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, disabled
>
>

`value`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={},`` ``label='Value')`
A dictionary containing the uploaded file(s) as bytes or string objects
indexed by the filename. Files that have a text/\* mimetype will
automatically be decoded as utf-8.

`width`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``default=300,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of this component. If sizing_mode is set to stretch or scale mode
this will merely be used as a suggestion.

`accepted_filetypes`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'str'>,`` ``label='Accepted`` ``filetypes')`
List of accepted file types. Can be mime types, file extensions or wild
cards.For instance \[‘image/[\*](#id3)’\] will accept all images.
\[‘.png’, ‘image/jpeg’\] will only accepts PNGs and JPEGs.

`chunk_size`` ``=`` ``Integer(default=10000000,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Chunk`` ``size')`
Size in bytes per chunk transferred across the WebSocket.

`layout`` ``=`` ``Selector(label='Layout',`` ``names={},`` ``objects=['circle',`` ``'compact',`` ``'integrated'])`
Compact mode removes padding. Integrated mode renders FilePond as part
of a bigger element. Circle mode keeps FilePond’s per-file action
buttons and upload progress indicator inside the circular drop area.

`max_file_size`` ``=`` ``String(allow_None=True,`` ``label='Max`` ``file`` ``size')`
Maximum size of a file as a string with units given in KB or MB, e.g.
5MB or 750KB.

`max_files`` ``=`` ``Integer(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Max`` ``files')`
Maximum number of files that can be uploaded if multiple=True.

`max_total_file_size`` ``=`` ``String(allow_None=True,`` ``label='Max`` ``total`` ``file`` ``size')`
Maximum size of all uploaded files, as a string with units given in KB
or MB, e.g. 5MB or 750KB.

`mime_type`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={},`` ``label='Mime`` ``type')`
A dictionary containing the mimetypes for each of the uploaded files
indexed by their filename.

`multiple`` ``=`` ``Boolean(default=False,`` ``label='Multiple')`
Whether to allow uploading multiple files.

`previews`` ``=`` ``ListSelector(default=['image',`` ``'pdf'],`` ``label='Previews',`` ``names={},`` ``objects=['image',`` ``'pdf'])`
List of previews to enable in the FileDropper. The following previews
are available: - image: Adds support for image previews. - pdf: Adds
support for PDF previews.

class panel.ui.widgets.FileInput(\*, chunk_size, max_file_size, max_total_file_size, uploaded_label, clicks, disable_elevation, end_icon, icon, icon_size, size, description_delay, attached, dark_theme, sx, theme_config, use_shadow_dom, button_style, button_type, color, variant, accept, description, directory, filename, mime_type, multiple, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_FileUploadArea`,
`_ButtonBase`,
[FileInput](panel.widgets.input.md#panel.widgets.input.FileInput)

The FileInput allows the user to upload one or more files to the server.

It makes the filename, MIME type and (bytes) content available in
Python.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/FileInput.html](https://panel-material-ui.holoviz.org/reference/widgets/FileInput.html)

- [https://panel.holoviz.org/reference/widgets/FileInput.html](https://panel.holoviz.org/reference/widgets/FileInput.html)

- [https://mui.com/material-ui/react-button/#file-upload](https://mui.com/material-ui/react-button/#file-upload)

Example:

\>\>\> FileInput(accept='.png,.jpeg', multiple=True)\

Methods

|  |  |
|----|----|
| [clear](#panel.ui.widgets.FileInput.clear)() | Clear the file(s) in the FileInput widget |
| [object](#panel.ui.widgets.FileInput.object)() | Returns the currently uploaded file(s) as a viewable Python object or list of viewable Python objects. |
| [save](#panel.ui.widgets.FileInput.save)(filename) | Saves the uploaded FileInput data object(s) to file(s) or BytesIO object(s). |
| [view](#panel.ui.widgets.FileInput.view)(\*\[, object_if_no_value, layout\]) | Create a bound Panel component for viewing the uploaded file(s). |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.input.FileInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets. input .FileInput](panel.widgets.input.md#panel.widgets.input.FileInput):
> value, accept, directory, filename, mime_type, multiple
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
> label, margin, attached, disabled
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_style, button_type, color, description_delay
>
> `panel_material_ui.widgets.button._ButtonBase`:
> variant, clicks, disable_elevation, end_icon, icon, icon_size, size
>
> `panel_material_ui.widgets.input._FileUploadArea`:
> chunk_size, max_file_size, max_total_file_size, uploaded_label
>
>

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of the button in pixels.

clear()
Clear the file(s) in the FileInput widget

object()
Returns the currently uploaded file(s) as a viewable Python object or
list of viewable Python objects.

For example an uploaded CSV file will return a Pandas DataFrame, an
uploaded MP3 file will return the path to a temporary file etc.

save(filename)
Saves the uploaded FileInput data object(s) to file(s) or BytesIO
object(s).

Parameters:
**filename (str or list\[str\]): File path or file-like object**

view(\*, object_if_no_value=None, layout=None, **kwargs)
Create a bound Panel component for viewing the uploaded file(s).

This method creates a view of the currently uploaded file(s). It updates
when the uploaded file value changes.

Parameters:
object_if_no_value : Displayble Python object, optional
Object to display when no files are uploaded. If None, an invisible
layout will be shown when no files are present.

layout : Panel layout class, optional
The layout class to use for organizing multiple file views. If None,
defaults to panel_material_ui.Tabs.

****kwargs**
Additional keyword arguments passed to the layout component.

Returns:
Panel bound function
A Panel bind object that reactively updates the file view when the
FileInput parameters change.

Examples

\>\>\> file_input = FileInput()\
\>\>\> file_view = file_input.view(layout=pmui.Column)\
\>\>\> \# The view will automatically update when files are uploaded\

width = None

class panel.ui.widgets.FileSelector(directory: str \| os.PathLike \| None = None, fs: AbstractFileSystem \| None = None, **params)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget),
[BaseFileSelector](panel.widgets.file_selector.md#panel.widgets.file_selector.BaseFileSelector)

The FileSelector widget allows browsing the filesystem on the server and
selecting one or more files in a directory.

The widget renders a Material UI file browser consisting of a navigation
toolbar (back, forward, up and reload), a breadcrumb trail and an
editable path field, a list of the entries in the current directory and
a collapsible summary of the current selection.

By default the directory the widget is initialized with also becomes the
root_directory, i.e. the boundary the user cannot navigate above. Since
the browser is a filesystem read primitive, always set root_directory
explicitly when serving a FileSelector to untrusted users.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/FileSelector.html](https://panel-material-ui.holoviz.org/reference/widgets/FileSelector.html)

- [https://panel.holoviz.org/reference/widgets/FileSelector.html](https://panel.holoviz.org/reference/widgets/FileSelector.html)

- [https://mui.com/material-ui/react-list/](https://mui.com/material-ui/react-list/)

Example:

\>\>\> FileSelector(directory='~', file_pattern='\*.png')\

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

`directory`` ``=`` ``String(default='/Users/runner/work/panel/panel',`` ``label='Directory')`
The directory to explore.

`file_pattern`` ``=`` ``String(default='*',`` ``label='File`` ``pattern')`
A glob-like pattern to filter the files.

`only_files`` ``=`` ``Boolean(default=False,`` ``label='Only`` ``files')`
Whether to only allow selecting files.

`refresh_period`` ``=`` ``Integer(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Refresh`` ``period')`
If set to non-None value indicates how frequently to refresh the
directory contents in milliseconds.

`root_directory`` ``=`` ``String(allow_None=True,`` ``label='Root`` ``directory')`
The root directory beyond which users cannot navigate. If not set it is
pinned to the directory the widget was initialized with.

`value`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=(<class`` ``'str'>,`` ``<class`` ``'pathlib.Path'>),`` ``label='Value')`
List of selected files.

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of the widget.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the checkboxes and links.

`show_hidden`` ``=`` ``Boolean(default=False,`` ``label='Show`` ``hidden')`
Whether to show hidden files and directories (starting with a period).

`size`` ``=`` ``Integer(default=10,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Size')`
The approximate number of entries shown at once, which bounds the height
of the entry list.

`_can_back`` ``=`` ``Boolean(default=False,`` ``label='`` ``can`` ``back')`
Whether the back button is enabled.

`_can_forward`` ``=`` ``Boolean(default=False,`` ``label='`` ``can`` ``forward')`
Whether the forward button is enabled.

`_can_up`` ``=`` ``Boolean(default=False,`` ``label='`` ``can`` ``up')`
Whether the up button is enabled.

`_crumbs`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'dict'>,`` ``label='`` ``crumbs')`
Breadcrumb trail from the root directory to the current directory.

`_items`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'dict'>,`` ``label='`` ``items')`
The entries in the current directory.

width = None

class panel.ui.widgets.FloatInput(\*, step, value_throttled, page_step_multiplier, wheel_wait, mode, end, format, placeholder, size, start, color, error_state, helper_text, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_SpinnerBase`,
`_FloatInputBase`

The FloatInput allows selecting an integer value using a spinbox.

It behaves like a slider except that lower and upper bounds are optional
and a specific value can be entered. The value can be changed using the
keyboard (up, down, page up, page down), mouse wheel and arrow buttons.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/FloatInput.html](https://panel-material-ui.holoviz.org/reference/widgets/FloatInput.html)

- [https://panel.holoviz.org/reference/widgets/FloatInput.html](https://panel.holoviz.org/reference/widgets/FloatInput.html)

Example:

\>\>\> FloatInput(label='Value', value=100, start=0, end=1000, step=10)\

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
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._NumericInputBase`:
> format, placeholder, size
>
> `panel_material_ui.widgets.input._FloatInputBase`:
> value, start, end, mode
>
> `panel_material_ui.widgets.input._SpinnerBase`:
> width, page_step_multiplier, wheel_wait
>
>

`step`` ``=`` ``Number(default=0.1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Step')`
The step size.

`value_throttled`` ``=`` ``Number(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``throttled')`
The current value. Updates only on \<enter\> or when the widget looses
focus.

class panel.ui.widgets.FloatSlider(\*, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_ContinuousSlider`

The FloatSlider widget allows selecting a floating-point value within a
set of bounds using a slider.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/FloatSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/FloatSlider.html)

- [https://panel.holoviz.org/reference/widgets/FloatSlider.html](https://panel.holoviz.org/reference/widgets/FloatSlider.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

Example:

\>\>\> FloatSlider(value=0.5, start=0.0, end=1.0, step=0.1, label="Float value")\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> value, bar_color, direction, tooltips, color, start, end, format,
> marks, size, track, value_label, value_throttled, inline_layout
>
>

`step`` ``=`` ``Number(default=0.1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Step')`
The step size.

class panel.ui.widgets.Gauge(\*, annulus_width, bounds, colors, custom_opts, end_angle, format, num_splits, show_labels, show_ticks, start_angle, title_size, tooltip_format, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [ValueIndicator](panel.widgets.indicators.md#panel.widgets.indicators.ValueIndicator)

A Gauge represents a value in some range as a position on speedometer or
gauge. It is similar to a Dial but visually a lot busier. Requires the
ECharts extension to be loaded.

Reference:
[https://panel.holoviz.org/reference/indicators/Gauge.html](https://panel.holoviz.org/reference/indicators/Gauge.html)

Example:

\>\>\> pn.extension('echarts')\
\>\>\> Gauge(label='Speed', value=79, bounds=(0, 200), colors=\[(0.4, 'green'), (1, 'red')\])\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> margin, disabled
>
> `panel.widgets.indicators.Indicator`:
> sizing_mode
>
>

`value`` ``=`` ``Number(allow_None=True,`` ``default=25,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
Value to indicate on the gauge a value within the declared bounds.

`height`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``default=300,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Height')`
The height of the component (in pixels). This can be either fixed or
preferred height, depending on height sizing policy.

`width`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``default=300,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
The width of the component (in pixels). This can be either fixed or
preferred width, depending on width sizing policy.

`annulus_width`` ``=`` ``Integer(default=10,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Annulus`` ``width')`
Width of the gauge annulus.

`bounds`` ``=`` ``Range(default=(0,`` ``100),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Bounds',`` ``length=2)`
The upper and lower bound of the dial.

`colors`` ``=`` ``List(allow_None=True,`` ``bounds=(0,`` ``None),`` ``item_type=<class`` ``'tuple'>,`` ``label='Colors')`
Color thresholds for the Gauge, specified as a list of tuples of the
fractional threshold and the color to switch to.

`custom_opts`` ``=`` ``Dict(allow_None=True,`` ``class_=<class`` ``'dict'>,`` ``label='Custom`` ``opts')`
Additional options to pass to the ECharts Gauge definition.

`end_angle`` ``=`` ``Number(default=-45,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End`` ``angle')`
Angle at which the gauge ends.

`format`` ``=`` ``String(default='{value}%',`` ``label='Format')`
Formatting string for the value indicator.

`num_splits`` ``=`` ``Integer(default=10,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Num`` ``splits')`
Number of splits along the gauge.

`show_ticks`` ``=`` ``Boolean(default=True,`` ``label='Show`` ``ticks')`
Whether to show ticks along the dials.

`show_labels`` ``=`` ``Boolean(default=True,`` ``label='Show`` ``labels')`
Whether to show tick labels along the dials.

`start_angle`` ``=`` ``Number(default=225,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Start`` ``angle')`
Angle at which the gauge starts.

`tooltip_format`` ``=`` ``String(default='{b}`` ``:`` ``{c}%',`` ``label='Tooltip`` ``format')`
Formatting string for the hover tooltip.

`title_size`` ``=`` ``Integer(allow_None=True,`` ``default=18,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Title`` ``size')`
Size of title font.

class panel.ui.widgets.Grammar(\*, src, uri, weight, name)
Bases: `Parameterized`

A set of words or patterns of words that we want the speech recognition
service to recognize

For example

grammar = Grammar(
src=’#JSGF V1.0; grammar colors; public \<color\> = aqua \| azure \|
beige;’, weight=0.7

)

Wraps the HTML SpeechGrammar API. See
[https://developer.mozilla.org/en-US/docs/Web/API/SpeechGrammar](https://developer.mozilla.org/en-US/docs/Web/API/SpeechGrammar)

Methods

|  |  |
|----|----|
| [serialize](#panel.ui.widgets.Grammar.serialize)() | Returns the grammar as dict |

**Parameter Definitions**

------------------------------------------------------------------------

`src`` ``=`` ``String(default='',`` ``label='Src')`
A set of words or patterns of words that we want the recognition service
to recognize. Defined using JSpeech Grammar Format. See
[https://www.w3.org/TR/jsgf/](https://www.w3.org/TR/jsgf/).

`uri`` ``=`` ``String(default='',`` ``label='Uri')`
An uri pointing to the definition. If src is available it will be used.
Otherwise uri. The uri will be loaded on the client side only.

`weight`` ``=`` ``Number(bounds=(0.0,`` ``1.0),`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Weight',`` ``step=0.01)`
The weight of the grammar. A number in the range 0–1. Default is 1.

serialize()
Returns the grammar as dict

class panel.ui.widgets.GrammarList(iterable=(), /)
Bases: `list`

A list of Grammar objects containing words or patterns of words that we
want the recognition service to recognize.

Example:

grammar = ‘#JSGF V1.0; grammar colors; public \<color\> = aqua \| azure
\| beige \| bisque ;’ grammar_list = GrammarList()
grammar_list.add_from_string(grammar, 1)

Wraps the HTML 5 SpeechGrammarList API

See [https://developer.mozilla.org/en-US/docs/Web/API/SpeechGrammarList](https://developer.mozilla.org/en-US/docs/Web/API/SpeechGrammarList)

Methods

|  |  |
|----|----|
| [serialize](#panel.ui.widgets.GrammarList.serialize)() | Returns a list of serialized grammars |

add_from_string(src, weight=1.0)
Takes a src and weight and adds it to the GrammarList as a new Grammar
object. The new Grammar object is returned.

add_from_uri(uri, weight=1.0)
Takes a grammar present at a specific uri, and adds it to the
GrammarList as a new Grammar object. The new Grammar object is returned.

serialize()
Returns a list of serialized grammars

class panel.ui.widgets.IconButton(\*, edge, href, target, toggle_duration, active_icon, clicks, disable_elevation, end_icon, icon, icon_size, size, description_delay, attached, description, dark_theme, sx, theme_config, use_shadow_dom, button_style, button_type, color, variant, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_ClickableIcon`,
`_ButtonBase`

The IconButton widget facilitates event triggering upon button clicks.

This widget displays a default icon initially. Upon being clicked, an
active_icon appears for a specified toggle_duration.

For instance, the IconButton can be effectively utilized to implement a
feature akin to ChatGPT’s copy-to-clipboard button.

The button incorporates a value attribute, which alternates between
False and True as the click event is processed.

Furthermore, it includes an clicks attribute, enabling subscription to
click events for further actions or monitoring.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/IconButton.html](https://panel-material-ui.holoviz.org/reference/widgets/IconButton.html)

- [https://panel.holoviz.org/reference/widgets/ButtonIcon.html](https://panel.holoviz.org/reference/widgets/ButtonIcon.html)

- [https://mui.com/material-ui/api/icon-button/](https://mui.com/material-ui/api/icon-button/)

Example:

\>\>\> button_icon = IconButton(\
...     icon='favorite',\
...     active_icon='check',\
...     description='Copy',\
...     toggle_duration=2000\
... )\

Methods

|  |  |
|----|----|
| [js_on_click](#panel.ui.widgets.IconButton.js_on_click)(\[args, code\]) | Allows defining a JS callback to be triggered when the button is clicked. |
| [jscallback](#panel.ui.widgets.IconButton.jscallback)(\[args\]) | Allows defining a Javascript (JS) callback to be triggered when a property changes on the source object. |
| [on_click](#panel.ui.widgets.IconButton.on_click)(callback) | Register a callback to be executed when the button is clicked. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
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
> label, margin, attached, disabled
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_style, button_type, color, description_delay
>
> `panel_material_ui.widgets.button._ButtonBase`:
> width, variant, disable_elevation, end_icon
>
> `panel_material_ui.widgets.icon._ClickableIcon`:
> active_icon, icon, icon_size, size
>
>

`value`` ``=`` ``Event(default=False,`` ``label='Value')`
Toggles from False to True while the event is being processed.

`clicks`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Clicks')`
The number of times the button has been clicked.

`edge`` ``=`` ``Selector(default=False,`` ``label='Edge',`` ``names={},`` ``objects=['start',`` ``'end',`` ``False])`
Whether the icon should be on the start or end of the button.

`href`` ``=`` ``String(allow_None=True,`` ``label='Href')`
The URL to navigate to when the button is clicked.

`target`` ``=`` ``Selector(default='_self',`` ``label='Target',`` ``names={},`` ``objects=['_blank',`` ``'_parent',`` ``'_self',`` ``'_top'])`
Where to open the linked document.

`toggle_duration`` ``=`` ``Integer(default=75,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Toggle`` ``duration')`
The number of milliseconds the active_icon should be shown for and how
long the button should be disabled for.

js_on_click(args: dict\[str, Any\] \| None = None, code: str = '') → Callback
Allows defining a JS callback to be triggered when the button is
clicked.

Parameters:
**args: dict**
A mapping of objects to make available to the JS callback

**code: str**
The Javascript code to execute when the button is clicked.

Returns:
callback: Callback
The Callback which can be used to disable the callback.

jscallback(args: dict\[str, Any\] \| None = None, **callbacks: str) → Callback
Allows defining a Javascript (JS) callback to be triggered when a
property changes on the source object. The keyword arguments define the
properties that trigger a callback and the JS code that gets executed.

Parameters:
**args: dict**
A mapping of objects to make available to the JS callback

****callbacks: dict**
A mapping between properties on the source model and the code to execute
when that property changes

Returns:
callback: Callback
The Callback which can be used to disable the callback.

on_click(callback: Callable\[\[Event\], None\]) → Watcher
Register a callback to be executed when the button is clicked.

The callback is given an Event argument declaring the number of clicks.

Returns:
watcher: param.Parameterized.Watcher
A Watcher that executes the callback when the MenuButton is clicked.

class panel.ui.widgets.IntInput(\*, step, value_throttled, page_step_multiplier, wheel_wait, mode, end, format, placeholder, size, start, color, error_state, helper_text, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_SpinnerBase`,
`_IntInputBase`

The IntInput allows selecting an integer value using a spinbox.

It behaves like a slider except that lower and upper bounds are optional
and a specific value can be entered. The value can be changed using the
keyboard (up, down, page up, page down), mouse wheel and arrow buttons.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/IntInput.html](https://panel-material-ui.holoviz.org/reference/widgets/IntInput.html)

- [https://panel.holoviz.org/reference/widgets/IntInput.html](https://panel.holoviz.org/reference/widgets/IntInput.html)

- [https://mui.com/material-ui/react-text-field/#input-adornments](https://mui.com/material-ui/react-text-field/#input-adornments)

Example:

\>\>\> IntInput(name='Value', value=100, start=0, end=1000, step=10)\

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
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._NumericInputBase`:
> format, placeholder, size
>
> `panel_material_ui.widgets.input._IntInputBase`:
> value, start, end, mode
>
> `panel_material_ui.widgets.input._SpinnerBase`:
> width, page_step_multiplier, wheel_wait
>
>

`step`` ``=`` ``Integer(default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Step')`
The step size.

`value_throttled`` ``=`` ``Integer(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``throttled')`
The current value. Updates only on \<enter\> or when the widget looses
focus.

class panel.ui.widgets.IntRangeSlider(\*, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_RangeSliderBase`

The IntRangeSlider widget allows selecting an integer range using a
slider with two handles.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/IntRangeSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/IntRangeSlider.html)

- [https://panel.holoviz.org/reference/widgets/IntRangeSlider.html](https://panel.holoviz.org/reference/widgets/IntRangeSlider.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

Example:

\>\>\> IntRangeSlider(\
...     value=(2, 4), start=0, end=10, step=2, label="A tuple of integers"\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> bar_color, direction, tooltips, color, marks, size, track,
> value_label, inline_layout
>
> `panel_material_ui.widgets.slider._RangeSliderBase`:
> value, value_throttled
>
>

`start`` ``=`` ``Integer(default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Start')`
The starting value of the slider.

`end`` ``=`` ``Integer(default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End')`
The ending value of the slider.

`format`` ``=`` ``ClassSelector(class_=(<class`` ``'str'>,`` ``<class`` ``'bokeh.models.formatters.TickFormatter'>),`` ``default='0,0',`` ``label='Format')`
A custom format string or Bokeh TickFormatter.

`step`` ``=`` ``Integer(default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Step')`
The step size for the slider.

`value_start`` ``=`` ``Integer(constant=True,`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``start',`` ``readonly=True)`
The lower value of the selected range.

`value_end`` ``=`` ``Integer(constant=True,`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``end',`` ``readonly=True)`
The upper value of the selected range.

class panel.ui.widgets.IntSlider(\*, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_ContinuousSlider`

The IntSlider widget allows selecting an integer value within a set of
bounds using a slider.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/IntSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/IntSlider.html)

- [https://panel.holoviz.org/reference/widgets/IntSlider.html](https://panel.holoviz.org/reference/widgets/IntSlider.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

Example:

\>\>\> IntSlider(value=5, start=0, end=10, step=1, label="Integer Value")\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> bar_color, direction, tooltips, color, marks, size, track,
> value_label, inline_layout
>
>

`value`` ``=`` ``Integer(default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
The widget value which the widget type resolves to when used as a
reactive param reference.

`start`` ``=`` ``Integer(default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Start')`
The starting value of the slider.

`end`` ``=`` ``Integer(default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End')`
The ending value of the slider.

`format`` ``=`` ``ClassSelector(class_=(<class`` ``'str'>,`` ``<class`` ``'bokeh.models.formatters.TickFormatter'>),`` ``default='0,0',`` ``label='Format')`
A custom format string or Bokeh TickFormatter.

`step`` ``=`` ``Integer(bounds=(1,`` ``None),`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Step')`
The step size for the slider.

`value_throttled`` ``=`` ``Integer(constant=True,`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``throttled')`
Throttled value for the slider.

class panel.ui.widgets.JSONEditor(**params: Any)
Bases: [Widget](panel.widgets.base.md#panel.widgets.base.Widget)

The JSONEditor provides a visual editor for JSON-serializable
datastructures, e.g. Python dictionaries and lists, with functionality
for different editing modes, inserting objects and validation using JSON
Schema.

Reference:
[https://panel.holoviz.org/reference/widgets/JSONEditor.html](https://panel.holoviz.org/reference/widgets/JSONEditor.html)

Example:

\>\>\> JSONEditor(value={\
...     'dict'  : {'key': 'value'},\
...     'float' : 3.14,\
...     'int'   : 1,\
...     'list'  : \[1, 2, 3\],\
...     'string': 'A string',\
... }, mode='code')\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
>

`value`` ``=`` ``Parameter(default={},`` ``label='Value')`
JSON data to be edited.

`menu`` ``=`` ``Boolean(default=True,`` ``label='Menu')`
Adds main menu bar - Contains format, sort, transform, search etc.
functionality. true by default. Applicable in all types of mode.

`mode`` ``=`` ``Selector(default='tree',`` ``label='Mode',`` ``names={},`` ``objects=['tree',`` ``'view',`` ``'form',`` ``'text',`` ``'preview'])`
Sets the editor mode. In ‘view’ mode, the data and datastructure is
read-only. In ‘form’ mode, only the value can be changed, the data
structure is read-only. Mode ‘code’ requires the Ace editor to be loaded
on the page. Mode ‘text’ shows the data as plain text. The ‘preview’
mode can handle large JSON documents up to 500 MiB. It shows a preview
of the data, and allows to transform, sort, filter, format, or compact
the data.

`search`` ``=`` ``Boolean(default=True,`` ``label='Search')`
Enables a search box in the upper right corner of the JSONEditor. true
by default. Only applicable when mode is ‘tree’, ‘view’, or ‘form’.

`selection`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'str'>,`` ``label='Selection')`
Current selection.

`schema`` ``=`` ``Dict(allow_None=True,`` ``class_=<class`` ``'dict'>,`` ``label='Schema')`
Validate the JSON object against a JSON schema. A JSON schema describes
the structure that a JSON object must have, like required properties or
the type that a value must have. See [http://json-schema.org/](http://json-schema.org/) for more
information.

`templates`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'dict'>,`` ``label='Templates')`
Array of templates that will appear in the context menu, Each template
is a json object precreated that can be added as a object value to any
node in your document.

class panel.ui.widgets.LinearGauge(\*, bounds, colors, default_color, format, horizontal, nan_format, needle_color, show_boundaries, tick_size, title_size, unfilled_color, value_size, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [ValueIndicator](panel.widgets.indicators.md#panel.widgets.indicators.ValueIndicator)

A LinearGauge represents a value in some range as a position on an
linear scale. It is similar to a Dial/Gauge but visually more compact.

Reference: [https://panel.holoviz.org/reference/indicators/LinearGauge.html](https://panel.holoviz.org/reference/indicators/LinearGauge.html)

Example:

\>\>\> LinearGauge(value=30, default_color='red', bounds=(0, 100))\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> margin, disabled
>
> `panel.widgets.indicators.Indicator`:
> sizing_mode
>
>

`value`` ``=`` ``Number(allow_None=True,`` ``default=25,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
Value to indicate on the dial a value within the declared bounds.

`height`` ``=`` ``Integer(allow_None=True,`` ``bounds=(1,`` ``None),`` ``default=300,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Height')`
The height of the component (in pixels). This can be either fixed or
preferred height, depending on height sizing policy.

`width`` ``=`` ``Integer(allow_None=True,`` ``bounds=(1,`` ``None),`` ``default=125,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
The width of the component (in pixels). This can be either fixed or
preferred width, depending on width sizing policy.

`bounds`` ``=`` ``Range(default=(0,`` ``100),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Bounds',`` ``length=2)`
The upper and lower bound of the gauge.

`default_color`` ``=`` ``String(default='lightblue',`` ``label='Default`` ``color')`
Color of the radial annulus if not color thresholds are supplied.

`colors`` ``=`` ``Parameter(allow_None=True,`` ``label='Colors')`
Color thresholds for the gauge, specified as a list of tuples of the
fractional threshold and the color to switch to.

`format`` ``=`` ``String(default='{value:.2f}%',`` ``label='Format')`
Formatting string for the value indicator and lower/upper bounds.

`horizontal`` ``=`` ``Boolean(default=False,`` ``label='Horizontal')`
Whether to display the linear gauge horizontally.

`nan_format`` ``=`` ``String(default='-',`` ``label='Nan`` ``format')`
How to format nan values.

`needle_color`` ``=`` ``String(allow_None=True,`` ``label='Needle`` ``color')`
Color of the gauge needle. Defaults to black, or white in the dark
theme.

`show_boundaries`` ``=`` ``Boolean(default=False,`` ``label='Show`` ``boundaries')`
Whether to show the boundaries between colored regions.

`unfilled_color`` ``=`` ``String(allow_None=True,`` ``label='Unfilled`` ``color')`
Color of the unfilled region of the LinearGauge. Defaults to a light or
dark grey depending on the theme.

`title_size`` ``=`` ``String(allow_None=True,`` ``label='Title`` ``size')`
Font size of the gauge title.

`tick_size`` ``=`` ``String(allow_None=True,`` ``label='Tick`` ``size')`
Font size of the gauge tick labels.

`value_size`` ``=`` ``String(allow_None=True,`` ``label='Value`` ``size')`
Font size of the gauge value label.

class panel.ui.widgets.LinearProgress(\*, active, color, max, value_buffer, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget)

The LinearProgress widget displays the progress towards some target
based on the current value and the max value.

References:

- [https://panel-material-ui.holoviz.org/reference/indicators/Progress.html](https://panel-material-ui.holoviz.org/reference/indicators/Progress.html)

- [https://panel.holoviz.org/reference/indicators/LinearProgress.html](https://panel.holoviz.org/reference/indicators/LinearProgress.html)

- [https://mui.com/material-ui/react-progress/#linear](https://mui.com/material-ui/react-progress/#linear)

Example:

\>\>\> LinearProgress(value=20, color="primary")\

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
> label, margin, width, attached, description, disabled
>
>

`value`` ``=`` ``Number(bounds=(-1,`` ``None),`` ``default=-1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
The value of the progress bar.

`active`` ``=`` ``Boolean(default=True,`` ``label='Active')`
Whether to animate the bar when in indeterminate mode.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the progress bar.

`max`` ``=`` ``Number(bounds=(0,`` ``None),`` ``default=100,`` ``inclusive_bounds=(False,`` ``True),`` ``label='Max')`
Maximum progress value.

`value_buffer`` ``=`` ``Number(bounds=(-1,`` ``None),`` ``default=-1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value`` ``buffer')`
The buffer of the progress bar (if variant=”buffer”).

`variant`` ``=`` ``Selector(default='determinate',`` ``label='Variant',`` ``names={},`` ``objects=['determinate',`` ``'indeterminate',`` ``'buffer',`` ``'query'])`
The variant of the progress bar.

class panel.ui.widgets.ListInput(\*, enter_pressed, max_length, size, color, error_state, helper_text, variant, attached, dark_theme, sx, theme_config, use_shadow_dom, description, placeholder, serializer, type, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases:
[LiteralInput](#panel.ui.widgets.LiteralInput)

The ListInput allows entering a list value using a text input box.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal"
> title="panel.widgets.input.LiteralInput"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets. input .LiteralInput](panel.widgets.input.md#panel.widgets.input.LiteralInput):
> serializer
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._TextInputBase`:
> max_length, placeholder, size
>
> [title="panel_material_ui.widgets.input.TextInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets. input .TextInput](#panel.ui.widgets.TextInput):
> enter_pressed
>
> [title="panel_material_ui.widgets.input.LiteralInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets. input .LiteralInput](#panel.ui.widgets.LiteralInput):
> value_input
>
>

`value`` ``=`` ``Parameter(default=[],`` ``label='Value')`
The widget value which the widget type resolves to when used as a
reactive param reference.

`type`` ``=`` ``ClassSelector(class_=<class`` ``'type'>,`` ``constant=True,`` ``default=<class`` ``'list'>,`` ``label='Type',`` ``readonly=True)`
The type of the value.

type
alias of `list`

class panel.ui.widgets.LiteralInput(\*, enter_pressed, max_length, size, color, error_state, helper_text, variant, attached, dark_theme, sx, theme_config, use_shadow_dom, description, placeholder, serializer, type, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [TextInput](#panel.ui.widgets.TextInput),
[LiteralInput](panel.widgets.input.md#panel.widgets.input.LiteralInput)

The LiteralInput allows entering any string using a text input box.

References:

- [https://panel.holoviz.org/reference/widgets/LiteralInput.html](https://panel.holoviz.org/reference/widgets/LiteralInput.html)

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal"
> title="panel.widgets.input.LiteralInput"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets. input .LiteralInput](panel.widgets.input.md#panel.widgets.input.LiteralInput):
> serializer, type
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._TextInputBase`:
> max_length, placeholder, size
>
> [title="panel_material_ui.widgets.input.TextInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets. input .TextInput](#panel.ui.widgets.TextInput):
> enter_pressed
>
>

`value`` ``=`` ``Parameter(allow_None=True,`` ``default='',`` ``label='Value')`
The widget value which the widget type resolves to when used as a
reactive param reference.

`value_input`` ``=`` ``Parameter(allow_None=True,`` ``constant=True,`` ``default='',`` ``label='Value`` ``input',`` ``readonly=True)`
Initial or entered text value updated on every key press.

panel.ui.widgets.LoadingSpinner
alias of
[CircularProgress](#panel.ui.widgets.CircularProgress)

class panel.ui.widgets.MenuBar(\*, color, size, variant, active, items, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `NestedMenuBase`

The MenuBar component provides a horizontal application menu bar,
similar to those found in desktop applications (File, Edit, View, Help,
etc.). It supports nested submenus, keyboard shortcut hints, icons,
checkboxes, radio groups, item groups, and dividers.

The top-level items list defines the menu triggers (buttons) in the bar.
Each top-level item should have:

- label (str, required): The button text.

- icon (str, optional): Icon displayed before the label.

- disabled (bool, optional): Whether the menu is disabled.

- items (list\[dict\], required): The dropdown items for this menu.

Each dropdown item can be:

- A regular item: {‘label’: ‘Save’, ‘icon’: ‘save’, ‘hint’: ‘Ctrl+S’}

- A divider: None or {‘label’: ‘—‘}

- A submenu: {‘label’: ‘Share’, ‘icon’: ‘share’, ‘items’: \[…\]}

- A group header: {‘label’: ‘Alignment’, ‘group’: True, ‘items’: \[…\]}

- A checkbox item: {‘label’: ‘Show Toolbar’, ‘checkbox’: True}

- A radio item: {‘label’: ‘Light’, ‘radio’: ‘light’}

Radio items within a group share state: selecting one deselects the
others.

References:

- [https://panel-material-ui.holoviz.org/reference/menus/MenuBar.html](https://panel-material-ui.holoviz.org/reference/menus/MenuBar.html)

- [https://mui.com/material-ui/react-menubar/](https://mui.com/material-ui/react-menubar/)

Example:

\>\>\> pmui.MenuBar(items=\[\
...     {'label': 'File', 'items': \[\
...         {'label': 'New', 'icon': 'note_add', 'hint': 'Ctrl+N'},\
...         {'label': 'Open', 'icon': 'folder_open', 'hint': 'Ctrl+O'},\
...         {'label': 'Save', 'icon': 'save', 'hint': 'Ctrl+S'},\
...         None,\
...         {'label': 'Exit', 'icon': 'close'},\
...     \]},\
...     {'label': 'Edit', 'items': \[\
...         {'label': 'Undo', 'icon': 'undo', 'hint': 'Ctrl+Z'},\
...         {'label': 'Redo', 'icon': 'redo', 'hint': 'Ctrl+Y'},\
...     \]},\
... \])\

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
> label, attached, description, disabled
>
> `panel_material_ui.widgets.menus.MenuBase`:
> value, margin, items
>
> `panel_material_ui.widgets.menus.NestedMenuBase`:
> active
>
>

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
The width of the menu bar.

`color`` ``=`` ``Selector(default='default',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the menu bar buttons.

`size`` ``=`` ``Selector(default='small',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The size of the menu bar buttons.

`variant`` ``=`` ``Selector(default='elevation',`` ``label='Variant',`` ``names={},`` ``objects=['elevation',`` ``'outlined'])`
The visual variant of the menu bar container.

width = None

class panel.ui.widgets.MenuButton(\*, active, items, clicks, disable_elevation, end_icon, icon, icon_size, size, description_delay, attached, description, dark_theme, sx, theme_config, use_shadow_dom, button_style, button_type, color, variant, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MenuBase`,
`_ButtonBase`

The MenuButton component is a button component that allows selecting
from a list of items.

MenuButton items can be strings or objects with properties:
- label: The label of the menu button item (required)

- icon: The icon of the menu button item (optional)

- color: The color of the menu button item (optional)

- href: The URL to navigate to when the menu button item is clicked
  (optional)

- target: The target to open the URL in (optional)

- tooltip: The tooltip text shown on hover (optional)

References:

- [https://panel-material-ui.holoviz.org/reference/menus/MenuButton.html](https://panel-material-ui.holoviz.org/reference/menus/MenuButton.html)

- [https://mui.com/material-ui/react-menu-button/](https://mui.com/material-ui/react-menu-button/)

Example:

\>\>\> pmui.MenuButton(items=\[\
...     {'label': 'Open', 'icon': 'description'},\
...     {'label': 'Save', 'icon': 'save'},\
...     {'label': 'Exit', 'icon': 'close'},\
... \], label='File', icon='storage')\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
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
> label, attached, disabled
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_style, button_type, color, description_delay
>
> `panel_material_ui.widgets.button._ButtonBase`:
> variant, clicks, end_icon, icon, icon_size
>
> `panel_material_ui.widgets.menus.MenuBase`:
> value, width, active, items
>
>

`margin`` ``=`` ``Margin(allow_None=True,`` ``allow_refs=True,`` ``default=(5,`` ``10),`` ``label='Margin')`
Margin around the widget.

`disable_elevation`` ``=`` ``Boolean(default=False,`` ``label='Disable`` ``elevation')`
Removes the menu’s box-shadow for a flat appearance.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The size of the menu button.

class panel.ui.widgets.MenuList(\*, collapsed, color, dense, drag_type, draggable, highlight, removable, expanded, level_indent, show_children, active, items, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `TreeLikeBase`

The MenuList component is used to display a structured group of items,
such as menus, navigation links, or settings.

List items can be strings or objects with properties:
- label: The label of the list item (required)

- secondary: The secondary text of the list item (optional)

- icon: The icon of the list item (optional)

- avatar: The avatar of the list item (optional)

- color: The color of the list item (optional)

- actions: Actions to display on the list item (optional)

- items: Nested items (optional)

- selectable: Whether the list item is selectable (optional)

- href: The URL to navigate to when the list item is clicked (optional)

- target: The target to open the URL in (optional)

- tooltip: The tooltip text shown on hover (optional)

- draggable: Whether the item can be dragged, overriding draggable
  (optional)

References:

- [https://panel-material-ui.holoviz.org/reference/menus/MenuList.html](https://panel-material-ui.holoviz.org/reference/menus/MenuList.html)

- [https://mui.com/material-ui/react-list/](https://mui.com/material-ui/react-list/)

Example:

\>\>\> pmui.MenuList(items=\[\
...     {'label': 'Home', 'icon': 'home', 'secondary': 'Overview page'},\
...     {'label': 'Gallery', 'icon': 'image', 'secondary': 'Visual overview'},\
...     {'label': 'API', 'icon': 'code', 'secondary': 'API Reference'},\
...     {'label': 'About', 'icon': 'info'},\
... \], active=3)\

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
> label, attached, description, disabled
>
> `panel_material_ui.widgets.menus.MenuBase`:
> value, margin, width, items
>
> `panel_material_ui.widgets.menus.NestedMenuBase`:
> active
>
> `panel_material_ui.widgets.menus.TreeLikeBase`:
> expanded, level_indent, show_children
>
>

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the selected list item.

`collapsed`` ``=`` ``Boolean(default=False,`` ``label='Collapsed')`
Whether to collapse the tree to show only the icons and no child items.

`dense`` ``=`` ``Boolean(default=True,`` ``label='Dense')`
Whether to show the list items in a dense format.

`drag_type`` ``=`` ``String(default='application/x-pmui-menu-item',`` ``label='Drag`` ``type')`
MIME type under which a dragged item’s payload is set, so drop targets
can accept items from specific lists only.

`draggable`` ``=`` ``Boolean(default=False,`` ``label='Draggable')`
Whether items can be dragged. A dragged item carries
`{"path":`` ``[...],`` ``"label":`` ``...}`
as JSON under `drag_type`. An item’s own
`draggable` key overrides this.

`highlight`` ``=`` ``Boolean(default=True,`` ``label='Highlight')`
Whether to highlight the currently selected menu item.

`removable`` ``=`` ``Boolean(default=False,`` ``label='Removable')`
Whether to allow deleting items.

class panel.ui.widgets.MenuToggle(\*, persistent, toggle_icon, toggled, active, items, clicks, disable_elevation, end_icon, icon, icon_size, size, description_delay, attached, description, dark_theme, sx, theme_config, use_shadow_dom, button_style, button_type, color, variant, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MenuBase`,
`_ButtonBase`

The MenuToggle component is a menu button where individual items can be
toggled on/off.

Unlike MenuButton, MenuToggle allows each menu item to have a toggle
state with different icons for active/inactive states (e.g.,
filled/unfilled heart for favorites).

MenuToggle items can be strings or objects with properties:
- label: The label of the menu toggle item (required)

- icon: The icon when item is not toggled (optional)

- active_icon: The icon when item is toggled (optional)

- toggled: Whether the item is currently toggled (optional, default:
  false)

- color: The color of the menu toggle item (optional)

- active_color: The color when toggled (optional)

- tooltip: The tooltip text shown on hover (optional)

References:

- [https://panel-material-ui.holoviz.org/reference/menus/MenuToggle.html](https://panel-material-ui.holoviz.org/reference/menus/MenuToggle.html)

- [https://mui.com/material-ui/react-toggle-button/](https://mui.com/material-ui/react-toggle-button/)

Example:

\>\>\> pmui.MenuToggle(items=\[\
...     {'label': 'Favorite', 'icon': 'favorite_border', 'active_icon': 'favorite', 'toggled': False},\
...     {'label': 'Bookmark', 'icon': 'bookmark_border', 'active_icon': 'bookmark', 'toggled': True},\
...     {'label': 'Star', 'icon': 'star_border', 'active_icon': 'star', 'toggled': False},\
... \], label='Actions', icon='more_vert')\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
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
> label, attached, disabled
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_style, button_type, color, description_delay
>
> `panel_material_ui.widgets.button._ButtonBase`:
> variant, clicks, disable_elevation, end_icon, icon, icon_size
>
> `panel_material_ui.widgets.menus.MenuBase`:
> value, width, active, items
>
>

`margin`` ``=`` ``Margin(allow_None=True,`` ``allow_refs=True,`` ``default=5,`` ``label='Margin')`
Margin around the widget.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The size of the menu toggle.

`toggle_icon`` ``=`` ``String(allow_None=True,`` ``label='Toggle`` ``icon')`
Icon to display when menu is open (if different from base icon).

`toggled`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Toggled')`
List of indices of currently toggled items.

`persistent`` ``=`` ``Boolean(default=True,`` ``label='Persistent')`
Whether the menu stays open after toggling an item.

class panel.ui.widgets.MultiChoice(\*, chip, delete_button, option_limit, placeholder, search_option_limit, solid, bookmarks, disabled_options, dropdown_height, dropdown_open, filter_on_search, filter_str, searchable, value_label, color, error_state, helper_text, max_items, size, variant, visual_size, attached, dark_theme, sx, theme_config, use_shadow_dom, description, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_SelectDropdownBase`,
[MultiSelect](#panel.ui.widgets.MultiSelect)

The MultiChoice widget allows selecting multiple values from a list of
options.

It falls into the broad category of multi-value, option-selection
widgets that provide a compatible API and include the MultiSelect,
CrossSelector, CheckBoxGroup and CheckButtonGroup widgets.

The MultiChoice widget provides a much more compact UI than MultiSelect.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/MultiChoice.html](https://panel-material-ui.holoviz.org/reference/widgets/MultiChoice.html)

- [https://panel.holoviz.org/reference/widgets/MultiChoice.html](https://panel.holoviz.org/reference/widgets/MultiChoice.html)

- [https://mui.com/material-ui/react-select/#multiple-select](https://mui.com/material-ui/react-select/#multiple-select)

Example:

\>\>\> MultiChoice(\
...     label='Favourites', value=\['Panel', 'hvPlot'\],\
...     options=\['Panel', 'hvPlot', 'HoloViews', 'GeoViews', 'Datashader', 'Param', 'Colorcet'\],\
...     max_items=2\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
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
> label, margin, width, attached, description, disabled
>
> [title="panel_material_ui.widgets.select.MultiSelect"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets.select.MultiSelect](#panel.ui.widgets.MultiSelect):
> value, color, error_state, helper_text, max_items, size, visual_size,
> variant
>
> `panel_material_ui.widgets.select._SelectDropdownBase`:
> bookmarks, disabled_options, filter_str, filter_on_search,
> dropdown_height, dropdown_open, searchable, value_label
>
>

`chip`` ``=`` ``Boolean(default=True,`` ``label='Chip')`
Whether to display a chip for each selected option

`delete_button`` ``=`` ``Boolean(default=True,`` ``label='Delete`` ``button')`
Whether to display a button to delete a selected option.

`option_limit`` ``=`` ``Integer(allow_None=True,`` ``bounds=(1,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Option`` ``limit')`
Maximum number of options to display at once.

`search_option_limit`` ``=`` ``Integer(allow_None=True,`` ``bounds=(1,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Search`` ``option`` ``limit')`
Maximum number of options to display at once if search string is
entered.

`placeholder`` ``=`` ``String(default='',`` ``label='Placeholder')`
String displayed when no selection has been made.

`solid`` ``=`` ``Boolean(default=True,`` ``label='Solid')`
Whether to display chips with solid or outlined style.

class panel.ui.widgets.MultiPill(\*, color, disabled_options, max_items, size, variant, attached, dark_theme, sx, theme_config, use_shadow_dom, description, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MaterialMultiSelectBase`

The MultiPill widget allows selecting multiple values from a list of
options rendered as clickable pills.

It falls into the broad category of multi-value, option-selection
widgets that provide a compatible API and include the MultiSelect,
MultiChoice, CheckBoxGroup and CheckButtonGroup widgets.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/MultiPill.html](https://panel-material-ui.holoviz.org/reference/widgets/MultiPill.html)

- [https://panel.holoviz.org/reference/widgets/MultiPill.html](https://panel.holoviz.org/reference/widgets/MultiPill.html)

- [https://mui.com/material-ui/react-chip/](https://mui.com/material-ui/react-chip/)

Example:

\>\>\> MultiPill(label="Favourites", value=\["Panel", "hvPlot"\],\
...     options=\["Panel", "hvPlot", "HoloViews", "GeoViews"\])\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.select.MaterialMultiSelectBase`:
> value
>
>

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of selected pills.

`disabled_options`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Disabled`` ``options',`` ``nested_refs=True)`
Optional list of `options` that are disabled,
i.e. unusable and un-clickable. If `options` is
a dictionary the list items have to correspond to the values in the
options dictionary.

`max_items`` ``=`` ``Integer(allow_None=True,`` ``bounds=(1,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Max`` ``items')`
Maximum number of options that can be selected.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
Size of the pills.

`variant`` ``=`` ``Selector(default='outlined',`` ``label='Variant',`` ``names={},`` ``objects=['filled',`` ``'outlined'])`
Variant style of the pills.

class panel.ui.widgets.MultiSelect(\*, color, error_state, helper_text, max_items, size, variant, visual_size, attached, dark_theme, sx, theme_config, use_shadow_dom, description, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MaterialMultiSelectBase`

The MultiSelect widget allows selecting multiple values from a list of
options.

It falls into the broad category of multi-value, option-selection
widgets that provide a compatible API and include the MultiSelect,
CrossSelector, CheckBoxGroup and CheckButtonGroup widgets.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/MultiSelect.html](https://panel-material-ui.holoviz.org/reference/widgets/MultiSelect.html)

- [https://panel.holoviz.org/reference/widgets/MultiSelect.html](https://panel.holoviz.org/reference/widgets/MultiSelect.html)

- [https://mui.com/material-ui/react-select/#multiple-select](https://mui.com/material-ui/react-select/#multiple-select)

\>\>\> pmui.MultiSelect(label='MultiSelect', value=\['Apple', 'Pear'\],\
...     options=\['Apple', 'Banana', 'Pear', 'Strawberry'\], size=8)\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
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
> label, margin, width, attached, description, disabled
>
>

`value`` ``=`` ``List(allow_None=True,`` ``bounds=(0,`` ``None),`` ``default=[],`` ``label='Value')`
The selected values.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
Color of the multi-select component.

`error_state`` ``=`` ``Boolean(default=False,`` ``label='Error`` ``state')`
Whether to display in error state.

`helper_text`` ``=`` ``String(default='',`` ``label='Helper`` ``text')`
Helper text displayed below the select field.

`max_items`` ``=`` ``Integer(allow_None=True,`` ``bounds=(1,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Max`` ``items')`
Maximum number of options that can be selected.

`size`` ``=`` ``Integer(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Size')`
The number of options to display at once. Controls the visible height of
the list area.

`visual_size`` ``=`` ``Selector(default='medium',`` ``label='Visual`` ``size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The visual size of the multi-select control.

`variant`` ``=`` ``Selector(default='outlined',`` ``label='Variant',`` ``names={},`` ``objects=['filled',`` ``'outlined',`` ``'standard'])`
Variant style of the multi-select component.

class panel.ui.widgets.NestedBreadcrumbs(\*, auto_descend, path, color, max_items, separator, active, items, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `NestedMenuBase`,
`BreadcrumbsBase`

The NestedBreadcrumbs component provides breadcrumb-style navigation for
hierarchical data. It extends standard breadcrumbs by allowing each
non-root segment to open a sibling selector menu via a chevron, enabling
users to navigate between branches at any level.

Nested breadcrumbs help users visualize their position in a nested
structure and move both upward (via breadcrumb clicks) and sideways (via
sibling menus).

Breadcrumb items are defined as objects with the following properties:

- label: The label of the breadcrumb item (required)

- icon: The icon of the breadcrumb item (optional)

- avatar: The avatar of the breadcrumb item (optional)

- href: Link to navigate to when clicking the breadcrumb item (optional)

- target: Link target (e.g. “\_blank”) (optional)

- items: List of nested child items (optional)

- selectable: Whether the item can be selected in sibling menus
  (optional, defaults to True)

- tooltip: The tooltip text shown on hover (optional)

References:

- [https://panel-material-ui.holoviz.org/reference/menus/NestedBreadcrumbs.html](https://panel-material-ui.holoviz.org/reference/menus/NestedBreadcrumbs.html)

- [https://mui.com/material-ui/react-breadcrumbs/](https://mui.com/material-ui/react-breadcrumbs/)

Example:

\>\>\> pmui.NestedBreadcrumbs(items=\[\
...     {\
...         'label': 'Projects', 'icon': 'folder', 'items': \[\
...             {'label': 'A', 'icon': 'category', 'items': \[\
...                 {'label': 'A1', 'icon': 'grain'},\
...                 {'label': 'A2', 'icon': 'grain'},\
...             \]},\
...             {'label': 'B', 'icon': 'category', 'items': \[\
...                 {'label': 'B1', 'icon': 'grain'},\
...             \]},\
...         \]\
...     }\
... \], active=(0,))\

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
> label, attached, description, disabled
>
> `panel_material_ui.widgets.menus.MenuBase`:
> value, margin, width, items
>
> `panel_material_ui.widgets.menus.BreadcrumbsBase`:
> color, max_items, separator
>
>

`active`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'int'>,`` ``<class`` ``'tuple'>),`` ``label='Active')`
The index of the currently selected item. Can be a tuple of indices for
nested items.

`auto_descend`` ``=`` ``Boolean(default=True,`` ``label='Auto`` ``descend')`
Whether to automatically descend through the first child of each
selected item when rendering the breadcrumb path. When
`True` (default), the component will
automatically extend the visible path by following first-child items
below the current selection. When `False`, the
last breadcrumb segment will instead display a “Select…” placeholder
with a chevron menu, allowing the user to pick a child manually.

`path`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=<class`` ``'tuple'>,`` ``label='Path')`
The tuple containing indices of the currently rendered path.

class panel.ui.widgets.NestedSelect(\*, \_levels, \_max_depth, \_widgets, layout, levels, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases:
[NestedSelect](panel.widgets.select.md#panel.widgets.select.NestedSelect)

The NestedSelect widget is composed of multiple widgets, where
subsequent select options depend on the parent’s value.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/NestedSelect.html](https://panel-material-ui.holoviz.org/reference/widgets/NestedSelect.html)

- [https://panel.holoviz.org/reference/widgets/NestedSelect.html](https://panel.holoviz.org/reference/widgets/NestedSelect.html)

- [https://mui.com/material-ui/react-select/](https://mui.com/material-ui/react-select/)

Example:

\>\>\> NestedSelect(\
...     options={\
...         "gfs": {"tmp": \[1000, 500\], "pcp": \[1000\]},\
...         "name": {"tmp": \[1000, 925, 850, 700, 500\], "pcp": \[1000\]},\
...     },\
...     levels=\["model", "var", "level"\],\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width
>
> [class="reference internal"
> title="panel.widgets.select.NestedSelect"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.NestedSelect](panel.widgets.select.md#panel.widgets.select.NestedSelect):
> value, disabled, layout, levels, options, \_widgets, \_max_depth,
> \_levels
>
>

class panel.ui.widgets.Number(\*, colors, default_color, font_size, format, nan_format, title_size, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [ValueIndicator](panel.widgets.indicators.md#panel.widgets.indicators.ValueIndicator)

The Number indicator renders the value as text optionally colored
according to the colors thresholds.

Reference:
[https://panel.holoviz.org/reference/indicators/Number.html](https://panel.holoviz.org/reference/indicators/Number.html)

Example:

\>\>\> Number(label='Rate', value=72, format='{value}%', colors=\[(80, 'green'), (100, 'red')\]\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
> `panel.widgets.indicators.Indicator`:
> sizing_mode
>
> href="panel.widgets.indicators.html#panel.widgets.indicators.ValueIndicator"
> class="reference internal"
> title="panel.widgets.indicators.ValueIndicator"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.indicators.ValueIndicator:
> value
>
>

`default_color`` ``=`` ``String(default='currentcolor',`` ``label='Default`` ``color')`
The color of the Number indicator if no colors are provided

`colors`` ``=`` ``List(allow_None=True,`` ``bounds=(0,`` ``None),`` ``item_type=<class`` ``'tuple'>,`` ``label='Colors')`
Color thresholds for the Number indicator, specified as a tuple of the
absolute thresholds and the color to switch to.

`format`` ``=`` ``String(default='{value}',`` ``label='Format')`
A formatter string which accepts a {value}.

`font_size`` ``=`` ``String(default='54pt',`` ``label='Font`` ``size')`
The size of number itself.

`nan_format`` ``=`` ``String(default='-',`` ``label='Nan`` ``format')`
How to format nan values.

`title_size`` ``=`` ``String(default='18pt',`` ``label='Title`` ``size')`
The size of the title given by the label.

class panel.ui.widgets.NumberInput(\*, page_step_multiplier, wheel_wait, end, format, placeholder, size, start, color, error_state, helper_text, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_SpinnerBase`

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
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._NumericInputBase`:
> value, format, placeholder, size, start, end
>
> `panel_material_ui.widgets.input._SpinnerBase`:
> width, page_step_multiplier, wheel_wait
>
>

class panel.ui.widgets.Pagination(\*, boundary_count, color, count, shape, show_first_button, show_last_button, sibling_count, size, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget)

The Pagination component allows selecting from a list of pages.

References:

- [https://panel-material-ui.holoviz.org/reference/menus/Pagination.html](https://panel-material-ui.holoviz.org/reference/menus/Pagination.html)

- [https://mui.com/material-ui/react-pagination/](https://mui.com/material-ui/react-pagination/)

Example:

\>\>\> pmui.Pagination(count=100)\

Methods

|  |  |
|----|----|
| [paginate](#panel.ui.widgets.Pagination.paginate)(objects, layout, page_size, **params) | Paginate the items based on the current page and page size. |

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

`value`` ``=`` ``Integer(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
The current zero-indexed page number.

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
The width of the pagination.

`boundary_count`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Boundary`` ``count')`
The number of boundary pages to show.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the pagination.

`count`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Count')`
The total number of pages.

`shape`` ``=`` ``Selector(default='circular',`` ``label='Shape',`` ``names={},`` ``objects=['circular',`` ``'rounded'])`
The shape of the pagination.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The size of the pagination.

`sibling_count`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Sibling`` ``count')`
The number of sibling pages to show.

`show_first_button`` ``=`` ``Boolean(default=False,`` ``label='Show`` ``first`` ``button')`
Whether to show the first button.

`show_last_button`` ``=`` ``Boolean(default=False,`` ``label='Show`` ``last`` ``button')`
Whether to show the last button.

`variant`` ``=`` ``Selector(default='text',`` ``label='Variant',`` ``names={},`` ``objects=['outlined',`` ``'text'])`
The variant of the pagination.

classmethod paginate(objects: list, layout: type\[ListLike\] = \<class 'panel.layout.base.Column'\>, page_size: int = 10, **params)
Paginate the items based on the current page and page size.

Parameters:
**objects: list**
The list of objects to paginate.

**layout: type\[LayoutBase\]**
The layout to use for the paginated items.

**page_size: int**
The number of items to display per page.

**params: dict**
Additional parameters to pass to the layout.

Returns:
layout
The layout with the paginated items.

width = None

class panel.ui.widgets.PasswordInput(\*, enter_pressed, max_length, placeholder, size, color, error_state, helper_text, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_TextInputBase`

The PasswordInput widget allows entering any string using an obfuscated
text input box.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/PasswordInput.html](https://panel-material-ui.holoviz.org/reference/widgets/PasswordInput.html)

- [https://panel.holoviz.org/reference/widgets/PasswordInput.html](https://panel.holoviz.org/reference/widgets/PasswordInput.html)

- [https://mui.com/material-ui/react-text-field/#input-adornments](https://mui.com/material-ui/react-text-field/#input-adornments)

Example:

\>\>\> PasswordInput(label='Password', placeholder='Enter your password here ...')\

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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._TextInputBase`:
> value, max_length, placeholder, size, value_input
>
>

`enter_pressed`` ``=`` ``Event(default=False,`` ``label='Enter`` ``pressed')`
Event when the enter key has been pressed.

class panel.ui.widgets.Pill(\*, color, disabled_options, size, variant, attached, description, dark_theme, sx, theme_config, use_shadow_dom, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MaterialSingleSelectBase`

The Pill widget allows selecting a single value from a list of options
rendered as clickable pills.

It falls into the broad category of single-value, option-selection
widgets that provide a compatible API and include the Select,
AutocompleteInput, RadioBoxGroup and RadioButtonGroup widgets.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/Pill.html](https://panel-material-ui.holoviz.org/reference/widgets/Pill.html)

- [https://panel.holoviz.org/reference/widgets/Pill.html](https://panel.holoviz.org/reference/widgets/Pill.html)

- [https://mui.com/material-ui/react-chip/](https://mui.com/material-ui/react-chip/)

Example:

\>\>\> Pill(label="Study", options=\["Biology", "Chemistry", "Physics"\])\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.select.MaterialSingleSelectBase`:
> value
>
>

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the selected pill.

`disabled_options`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Disabled`` ``options',`` ``nested_refs=True)`
Optional list of `options` that are disabled,
i.e. unusable and un-clickable. If `options` is
a dictionary the list items have to correspond to the values in the
options dictionary.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
Size of the pills.

`variant`` ``=`` ``Selector(default='outlined',`` ``label='Variant',`` ``names={},`` ``objects=['filled',`` ``'outlined'])`
Variant style of the pills.

class panel.ui.widgets.Player(\*, color, size, variant, attached, description, dark_theme, sx, theme_config, use_shadow_dom, end, start, value_throttled, direction, interval, loop_policy, preview_duration, scale_buttons, show_loop_controls, show_value, step, value_align, visible_buttons, visible_loop_options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_PlayerBase`,
[Player](panel.widgets.player.md#panel.widgets.player.Player)

The Player provides controls to play and skip through a number of frames
defined by explicit start and end values. The speed at which the widget
plays is defined by the interval (in milliseconds), but it is also
possible to skip frames using the step parameter.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/Player.html](https://panel-material-ui.holoviz.org/reference/widgets/Player.html)

- [https://panel.holoviz.org/reference/widgets/Player.html](https://panel.holoviz.org/reference/widgets/Player.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

Example:

\>\>\> Player(label='Frame', start=0, end=100, value=32, loop_policy='loop')\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.player.PlayerBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.player.PlayerBase](panel.widgets.player.md#panel.widgets.player.PlayerBase):
> direction, interval, loop_policy, preview_duration,
> show_loop_controls, show_value, step, value_align, scale_buttons,
> visible_buttons, visible_loop_options
>
> [class="reference internal" title="panel.widgets.player.Player"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.player.Player](panel.widgets.player.md#panel.widgets.player.Player):
> value, start, end, value_throttled
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
> `panel_material_ui.widgets.player._PlayerBase`:
> height, width, color, size, variant
>
>

panel.ui.widgets.Progress
alias of
[LinearProgress](#panel.ui.widgets.LinearProgress)

class panel.ui.widgets.RadioBoxGroup(\*, color, inline, label_placement, size, attached, description, dark_theme, sx, theme_config, use_shadow_dom, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_RadioGroup`,
`MaterialSingleSelectBase`

The RadioBoxGroup widget allows selecting a value from a list of
options.

It falls into the broad category of single-value, option-selection
widgets that provide a compatible API and include the AutocompleteInput,
Select and RadioButtonGroup widgets.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/RadioBoxGroup.html](https://panel-material-ui.holoviz.org/reference/widgets/RadioBoxGroup.html)

- [https://panel.holoviz.org/reference/widgets/RadioBoxGroup.html](https://panel.holoviz.org/reference/widgets/RadioBoxGroup.html)

- [https://mui.com/material-ui/react-radio-button/](https://mui.com/material-ui/react-radio-button/)

Example:

\>\>\> RadioBoxGroup(\
...     label='Study', options=\['Biology', 'Chemistry', 'Physics'\],\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
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
> `panel_material_ui.widgets.select._RadioGroup`:
> width, color, label_placement, size, inline
>
>

`value`` ``=`` ``Parameter(allow_None=True,`` ``label='Value')`
The selected value.

class panel.ui.widgets.RadioButtonGroup(\*, orientation, size, variant, button_style, button_type, color, description_delay, attached, description, dark_theme, sx, theme_config, use_shadow_dom, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_ButtonGroup`,
`MaterialSingleSelectBase`

The RadioButtonGroup widget allows selecting from a list or dictionary
of values using a set of toggle buttons.

It falls into the broad category of single-value, option-selection
widgets that provide a compatible API and include the AutocompleteInput,
Select, and RadioBoxGroup widgets.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/RadioButtonGroup.html](https://panel-material-ui.holoviz.org/reference/widgets/RadioButtonGroup.html)

- [https://panel.holoviz.org/reference/widgets/RadioButtonGroup.html](https://panel.holoviz.org/reference/widgets/RadioButtonGroup.html)

- [https://mui.com/material-ui/react-toggle-button/](https://mui.com/material-ui/react-toggle-button/)

Example:

\>\>\> RadioButtonGroup(\
...     label='Plotting library', options=\['Matplotlib', 'Bokeh', 'Plotly'\],\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
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
> label, margin, attached, disabled
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_style, button_type, color, description_delay
>
> `panel_material_ui.widgets.select._ButtonGroup`:
> width, orientation, size, variant
>
>

`value`` ``=`` ``Parameter(allow_None=True,`` ``label='Value')`
The selected value.

`active`` ``=`` ``Integer(allow_None=True,`` ``constant=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Active',`` ``readonly=True)`
Zero-based index of the selected option, or None if none is selected.

class panel.ui.widgets.RangeSlider(\*, color, end, format, inline_layout, marks, size, start, step, track, value_label, value_throttled, attached, description, dark_theme, sx, theme_config, use_shadow_dom, bar_color, direction, orientation, show_value, tooltips, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_RangeSliderBase`

The RangeSlider widget allows selecting a floating-point range using a
slider with two handles.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/RangeSlider.html](https://panel-material-ui.holoviz.org/reference/widgets/RangeSlider.html)

- [https://panel.holoviz.org/reference/widgets/RangeSlider.html](https://panel.holoviz.org/reference/widgets/RangeSlider.html)

- [https://mui.com/material-ui/react-slider/](https://mui.com/material-ui/react-slider/)

Example:

\>\>\> RangeSlider(\
...     value=(1.0, 1.5), start=0.0, end=2.0, step=0.25, label="A tuple of floats"\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> `panel.widgets.slider._SliderBase`:
> orientation, show_value
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.slider._ContinuousSlider`:
> bar_color, direction, tooltips, color, start, end, format, marks,
> size, track, value_label, inline_layout
>
> `panel_material_ui.widgets.slider._RangeSliderBase`:
> value, value_throttled, value_start, value_end
>
>

`step`` ``=`` ``Number(default=0.1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Step')`
The step size of the slider.

class panel.ui.widgets.Rating(\*, color, empty_icon, end, icon, only_selected, precision, readonly, size, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget)

The Rating slider widget allows users to select a rating value of their
own.

References:

- [https://mui.com/material-ui/react-rating/](https://mui.com/material-ui/react-rating/)

Example:

\>\>\> Rating(value=3, size="large", name="Rate the product")\

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

`value`` ``=`` ``Number(allow_None=True,`` ``bounds=(0,`` ``5),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Value')`
The widget value which the widget type resolves to when used as a
reactive param reference.

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of the widget.

`color`` ``=`` ``Selector(label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the ratings.

`end`` ``=`` ``Integer(bounds=(1,`` ``None),`` ``default=5,`` ``inclusive_bounds=(True,`` ``True),`` ``label='End')`
The maximum value for the rating.

`empty_icon`` ``=`` ``String(allow_None=True,`` ``label='Empty`` ``icon')`
The icon to render for a non-selected rating.

`icon`` ``=`` ``String(default='star',`` ``label='Icon')`
The icon to render for a selected rating.

`only_selected`` ``=`` ``Boolean(default=False,`` ``label='Only`` ``selected')`
Whether to highlight only the select value

`precision`` ``=`` ``Number(bounds=(0,`` ``1.0),`` ``default=1.0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Precision')`
The precision of the rating value. If set to 0.5, the rating can be set
to 0, 0.5, 1, 1.5, …, up to the end value.

`readonly`` ``=`` ``Boolean(default=False,`` ``label='Readonly')`
Whether the rating is read-only. If True, the user cannot change the
rating.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
Size of the rating icons.

width = None

class panel.ui.widgets.Select(\*, color, error_state, helper_text, variant, groups, size, bookmarks, disabled_options, dropdown_height, dropdown_open, filter_on_search, filter_str, searchable, value_label, attached, description, dark_theme, sx, theme_config, use_shadow_dom, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MaterialSingleSelectBase`,
[Select](panel.widgets.select.md#panel.widgets.select.Select),
`_SelectDropdownBase`

The Select widget allows selecting a value from a list.

It falls into the broad category of single-value, option-selection
widgets that provide a compatible API and include the AutocompleteInput,
RadioBoxGroup and RadioButtonGroup widgets.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/Select.html](https://panel-material-ui.holoviz.org/reference/widgets/Select.html)

- [https://panel.holoviz.org/reference/widgets/Select.html](https://panel.holoviz.org/reference/widgets/Select.html)

- [https://mui.com/material-ui/react-select/](https://mui.com/material-ui/react-select/)

Example:

\>\>\> Select(label='Study', options=\['Biology', 'Chemistry', 'Physics'\])\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
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
> label, margin, attached, disabled
>
> `panel_material_ui.widgets.select._SelectDropdownBase`:
> bookmarks, filter_str, filter_on_search, dropdown_height,
> dropdown_open, searchable, value_label
>
> [class="reference internal" title="panel.widgets.select.Select"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.Select](panel.widgets.select.md#panel.widgets.select.Select):
> width, description, disabled_options
>
> `panel_material_ui.widgets.select.MaterialSingleSelectBase`:
> value
>
>

`groups`` ``=`` ``Dict(allow_None=True,`` ``class_=<class`` ``'dict'>,`` ``label='Groups',`` ``nested_refs=True)`
Dictionary whose keys are used to visually group the options and whose
values are either a list or a dictionary of options to select from.
Mutually exclusive with `options` and valid
only if `size` is 1.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
Declares how many options are displayed at the same time. If set to 1
displays options as dropdown otherwise displays scrollable area.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the select widget.

`error_state`` ``=`` ``Boolean(default=False,`` ``label='Error`` ``state')`
Whether to display in error state.

`helper_text`` ``=`` ``String(default='',`` ``label='Helper`` ``text')`
Helper text displayed below the select field.

`variant`` ``=`` ``Selector(default='outlined',`` ``label='Variant',`` ``names={},`` ``objects=['filled',`` ``'outlined',`` ``'standard'])`
The variant style of the select widget.

class panel.ui.widgets.SpeechToText(\*, \_grammars, abort, audio_started, button_hide, button_not_started, button_started, button_type, color, continuous, grammars, interim_results, lang, max_alternatives, results, service_uri, sound_started, speech_started, start, started, stop, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [Widget](panel.widgets.base.md#panel.widgets.base.Widget)

The SpeechToText widget controls the speech recognition service of the
browser.

It wraps the HTML5 SpeechRecognition API. See [https://developer.mozilla.org/en-US/docs/Web/API/SpeechRecognition](https://developer.mozilla.org/en-US/docs/Web/API/SpeechRecognition)

Reference:
[https://panel.holoviz.org/reference/widgets/SpeechToText.html](https://panel.holoviz.org/reference/widgets/SpeechToText.html)

Example:

\>\>\> SpeechToText(color="light")\

This functionality is **experimental** and only supported by Chrome and
a few other browsers. Checkout
[https://caniuse.com/speech-recognition](https://caniuse.com/speech-recognition)
for a up to date list of browsers supporting the SpeechRecognition Api.
Or alternatively [https://developer.mozilla.org/en-US/docs/Web/API/SpeechRecognition#Browser_compatibility](https://developer.mozilla.org/en-US/docs/Web/API/SpeechRecognition#Browser_compatibility)

On some browsers, like Chrome, using Speech Recognition on a web page
involves a server-based recognition engine. Your audio is sent to a web
service for recognition processing, so it won’t work offline. Whether
this is secure and confidential enough for your use case is up to you to
evaluate.

Attributes:
[results_as_html](#panel.ui.widgets.SpeechToText.results_as_html)
Returns the results formatted as html

[results_deserialized](#panel.ui.widgets.SpeechToText.results_deserialized)
Returns the results as a List of RecognitionResults

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
>

`value`` ``=`` ``String(constant=True,`` ``default='')`
The transcipt of the highest confidence RecognitionAlternative of the
last RecognitionResult. Please note we strip the transcript for leading
spaces.

`abort`` ``=`` ``Event(default=False,`` ``label='Abort')`
Stops the speech recognition service from listening to incoming audio,
and doesn’t attempt to return a RecognitionResult.

`start`` ``=`` ``Event(default=False,`` ``label='Start')`
Starts the speech recognition service listening to incoming audio with
intent to recognize grammars associated with the current
SpeechRecognition.

`stop`` ``=`` ``Event(default=False,`` ``label='Stop')`
Stops the speech recognition service from listening to incoming audio,
and attempts to return a RecognitionResult using the audio captured so
far.

`lang`` ``=`` ``Selector(allow_None=True,`` ``default='',`` ``names={},`` ``objects=['',`` ``'af-ZA',`` ``'ar-AE',`` ``'ar-BH',`` ``'ar-DZ',`` ``'ar-EG',`` ``'ar-IL',`` ``'ar-IQ',`` ``'ar-JO',`` ``'ar-KW',`` ``'ar-LB',`` ``'ar-MA',`` ``'ar-OM',`` ``'ar-PS',`` ``'ar-QA',`` ``'ar-SA',`` ``'ar-TN',`` ``'bg-BG',`` ``'ca-ES',`` ``'cmn-Hans-CN',`` ``'cmn-Hans-HK',`` ``'cmn-Hant-TW',`` ``'cs-CZ',`` ``'da-DK',`` ``'de-DE',`` ``'el-GR',`` ``'en-AU',`` ``'en-CA',`` ``'en-GB',`` ``'en-IE',`` ``'en-IN',`` ``'en-NZ',`` ``'en-PH',`` ``'en-US',`` ``'en-ZA',`` ``'es-AR',`` ``'es-BO',`` ``'es-CL',`` ``'es-CO',`` ``'es-CR',`` ``'es-DO',`` ``'es-EC',`` ``'es-ES',`` ``'es-GT',`` ``'es-HN',`` ``'es-MX',`` ``'es-NI',`` ``'es-PA',`` ``'es-PE',`` ``'es-PR',`` ``'es-PY',`` ``'es-SV',`` ``'es-US',`` ``'es-UY',`` ``'es-VE',`` ``'eu-ES',`` ``'fa-IR',`` ``'fi-FI',`` ``'fil-PH',`` ``'fr-FR',`` ``'gl-ES',`` ``'he-IL',`` ``'hi-IN',`` ``'hr_HR',`` ``'hu-HU',`` ``'id-ID',`` ``'is-IS',`` ``'it-CH',`` ``'it-IT',`` ``'ja-JP',`` ``'ko-KR',`` ``'lt-LT',`` ``'ms-MY',`` ``'nb-NO',`` ``'nl-NL',`` ``'pl-PL',`` ``'pt-BR',`` ``'pt-PT',`` ``'ro-RO',`` ``'ru-RU',`` ``'sk-SK',`` ``'sl-SI',`` ``'sr-RS',`` ``'sv-SE',`` ``'th-TH',`` ``'tr-TR',`` ``'uk-UA',`` ``'vi-VN',`` ``'yue-Hant-HK',`` ``'zu-ZA'])`
The language of the current SpeechRecognition in BCP 47 format. For
example ‘en-US’. If not specified, this defaults to the HTML lang
attribute value, or the user agent’s language setting if that isn’t set
either.

`continuous`` ``=`` ``Boolean(default=False,`` ``label='Continuous')`
Controls whether continuous results are returned for each recognition,
or only a single result. Defaults to False

`interim_results`` ``=`` ``Boolean(default=False,`` ``label='Interim`` ``results')`
Controls whether interim results should be returned (True) or not
(False.) Interim results are results that are not yet final (e.g. the
RecognitionResult.is_final property is False).

`max_alternatives`` ``=`` ``Integer(bounds=(1,`` ``5),`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Max`` ``alternatives')`
Sets the maximum number of RecognitionAlternatives provided per result.
A number between 1 and 5. The default value is 1.

`service_uri`` ``=`` ``String(default='',`` ``label='Service`` ``uri')`
Specifies the location of the speech recognition service used by the
current SpeechRecognition to handle the actual recognition. The default
is the user agent’s default speech service.

`grammars`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=<class`` ``'panel.widgets.speech_to_text.GrammarList'>,`` ``label='Grammars')`
A GrammarList object that represents the grammars that will be
understood by the current SpeechRecognition service

`button_hide`` ``=`` ``Boolean(default=False)`
If True no button is shown. If False a toggle Start/ Stop button is
shown.

`button_type`` ``=`` ``Selector(default='light',`` ``label='Button`` ``type',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'success',`` ``'warning',`` ``'danger',`` ``'light',`` ``'light',`` ``'dark'])`
The button styling. The same value is exposed as
`color`.

`color`` ``=`` ``Selector(default='light',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'success',`` ``'warning',`` ``'danger',`` ``'light',`` ``'light',`` ``'dark'])`
Semantic color of the button; alias for
`button_type`.

`button_not_started`` ``=`` ``String(default='')`
The text to show on the button when the SpeechRecognition service is NOT
started. If ‘’ a *muted microphone* icon is shown.

`button_started`` ``=`` ``String(default='')`
The text to show on the button when the SpeechRecognition service is
started. If ‘’ a *muted microphone* icon is shown.

`started`` ``=`` ``Boolean(constant=True,`` ``default=False,`` ``label='Started')`
Returns True if the Speech Recognition Service is started and False
otherwise.

`audio_started`` ``=`` ``Boolean(constant=True,`` ``default=False,`` ``label='Audio`` ``started')`
Returns True if the Audio is started and False otherwise.

`sound_started`` ``=`` ``Boolean(constant=True,`` ``default=False,`` ``label='Sound`` ``started')`
Returns True if the Sound is started and False otherwise.

`speech_started`` ``=`` ``Boolean(constant=True,`` ``default=False,`` ``label='Speech`` ``started')`
Returns True if the the User has started speaking and False otherwise.

`results`` ``=`` ``List(bounds=(0,`` ``None),`` ``constant=True,`` ``default=[],`` ``item_type=<class`` ``'dict'>,`` ``label='Results')`
The results as a list of Dictionaries.

`_grammars`` ``=`` ``List(bounds=(0,`` ``None),`` ``constant=True,`` ``default=[],`` ``item_type=<class`` ``'dict'>,`` ``label='`` ``grammars')`
List used to transfer the serialized grammars from server to browser.

property results_as_html: str
Returns the results formatted as html

Convenience method for ease of use

property results_deserialized
Returns the results as a List of RecognitionResults

class panel.ui.widgets.SpeedDial(\*, color, direction, icon, open_icon, persistent_tooltips, size, active, items, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MenuBase`

The SpeedDial component is a menu component that allows selecting from a
list of items.

SpeedDial items can be strings or objects with properties:

- label: The label of the speed dial item (required)

- icon: The icon of the speed dial item (optional)

- avatar: The avatar of the speed dial item (optional)

- color: The color of the speed dial item (optional)

References:

- [https://panel-material-ui.holoviz.org/reference/menus/SpeedDial.html](https://panel-material-ui.holoviz.org/reference/menus/SpeedDial.html)

- [https://mui.com/material-ui/react-speed-dial/](https://mui.com/material-ui/react-speed-dial/)

Example:

\>\>\> pmui.SpeedDial(items=\[\
...     {'label': 'Camera', 'icon': 'camera'},\
...     {'label': 'Photos', 'icon': 'photo'},\
...     {'label': 'Documents', 'icon': 'article'},\
... \], active=2, margin=(50, 20))\

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
> label, attached, description, disabled
>
> `panel_material_ui.widgets.menus.MenuBase`:
> value, margin, width, active, items
>
>

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the menu.

`direction`` ``=`` ``Selector(default='right',`` ``label='Direction',`` ``names={},`` ``objects=['right',`` ``'left',`` ``'up',`` ``'down'])`
The direction of the menu.

`icon`` ``=`` ``String(allow_None=True,`` ``label='Icon')`
The icon to display when the menu is closed.

`open_icon`` ``=`` ``String(allow_None=True,`` ``label='Open`` ``icon')`
The icon to display when the menu is open.

`persistent_tooltips`` ``=`` ``Boolean(default=False,`` ``label='Persistent`` ``tooltips')`
Whether to show persistent tooltips next to the menu items.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The size of the dial.

class panel.ui.widgets.SplitButton(\*, mode, active, items, clicks, disable_elevation, end_icon, icon, icon_size, size, description_delay, attached, description, dark_theme, sx, theme_config, use_shadow_dom, button_style, button_type, color, variant, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MenuBase`,
`_ButtonBase`

The SplitButton component combines a button with a dropdown menu,
allowing users to quickly access a primary action and related
alternatives.

This component supports two modes:

- **\`split\`**: The main button performs a default action, while the
  dropdown lets users trigger related but independent actions.

- **\`select\`**: Users select an option from the dropdown, and the main
  button triggers the selected action when clicked.

Each menu item can be a string or a dictionary with the following keys:
- **\`label\`** (str, required): The text displayed for the menu item.

- **\`icon\`** (str, optional): An icon to display next to the label.

- **\`href\`** (str, optional): A URL to open when the menu item is
  clicked.

- **\`target\`** (str, optional): Where to open the linked URL (e.g.,
  \_blank).

- **\`tooltip\`** (str, optional): Tooltip text shown on hover.

The SplitButton is ideal for workflows where a primary action is most
common, but users may occasionally need to choose an alternative.

References:

- [https://panel-material-ui.holoviz.org/reference/menus/SplitButton.html](https://panel-material-ui.holoviz.org/reference/menus/SplitButton.html)

- [https://mui.com/material-ui/react-button-group/#split-button](https://mui.com/material-ui/react-button-group/#split-button)

Example:

\>\>\> pmui.SplitButton(items=\[\
...     {'label': 'Open'},\
...     {'label': 'Save'},\
... \], label='Save')\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
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
> label, attached, disabled
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_style, button_type, color, description_delay
>
> `panel_material_ui.widgets.button._ButtonBase`:
> variant, clicks, disable_elevation, end_icon, icon, icon_size, size
>
> `panel_material_ui.widgets.menus.MenuBase`:
> value, width, active, items
>
>

`margin`` ``=`` ``Margin(allow_None=True,`` ``allow_refs=True,`` ``default=5,`` ``label='Margin')`
Margin around the widget.

`mode`` ``=`` ``Selector(default='split',`` ``label='Mode',`` ``names={},`` ``objects=['split',`` ``'select'])`
Allows toggling button behavior between split mode (button click and
menu click actions raise events) and select mode (only button click
raise events).

class panel.ui.widgets.StaticText(\*, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget)

The StaticText widget displays a text value, but does not allow editing
it. String values are rendered as HTML, any other value is escaped.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/StaticText.html](https://panel-material-ui.holoviz.org/reference/widgets/StaticText.html)

- [https://panel.holoviz.org/reference/widgets/StaticText.html](https://panel.holoviz.org/reference/widgets/StaticText.html)

Example:

\>\>\> StaticText(label='Model', value='animagen2')\

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

`value`` ``=`` ``Parameter(allow_None=True,`` ``label='Value')`
The current value to be displayed.

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
Width of the widget, sized to its text by default like the classic
StaticText.

width = None

class panel.ui.widgets.StepperMenu(\*, alternative_label, back_text, color, connector, indicator, next_text, non_linear, orientation, position, variant, active, items, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MenuBase`

The StepperMenu displays progress through a sequence of numbered steps
and emits the active step as users navigate. It is a menu-style
indicator: it is driven by a declarative list of items and reports the
selection via the active and value parameters.

Two variants are available via variant: the default standard variant
renders a labelled horizontal strip of steps, while the compact variant
renders a minimal mobile-style bar with a dots, progress, or text
indicator and back/next navigation.

Step items can be strings or dictionaries with the following properties:

- label: The label of the step (required)

- icon: Icon name or inline SVG shown for pending steps (optional)

- active_icon: Icon shown when the step is active or completed; falls
  back to the filled version of icon when not provided (optional)

- completed: Whether the step is marked complete (optional)

- error: Whether the step is in an error state (optional)

- optional: Whether to show an “Optional” caption under the label
  (optional)

- disabled: Whether the step is disabled (optional)

- tooltip: The tooltip text shown on hover (optional)

References:

- [https://panel-material-ui.holoviz.org/reference/menus/StepperMenu.html](https://panel-material-ui.holoviz.org/reference/menus/StepperMenu.html)

- [https://mui.com/material-ui/react-stepper/](https://mui.com/material-ui/react-stepper/)

Example:

\>\>\> pmui.StepperMenu(items=\[\
...     {'label': 'Account', 'icon': 'person', 'completed': True},\
...     {'label': 'Shipping', 'icon': 'local_shipping'},\
...     {'label': 'Review', 'icon': 'check', 'optional': True},\
... \], active=1)\

Methods

|  |  |
|----|----|
| [back](#panel.ui.widgets.StepperMenu.back)() | Return to the previous step. |
| [next](#panel.ui.widgets.StepperMenu.next)() | Advance to the next step. |
| [reset](#panel.ui.widgets.StepperMenu.reset)() | Reset to the first step. |

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
> label, attached, description, disabled
>
> `panel_material_ui.widgets.menus.MenuBase`:
> value, margin, width, items
>
>

`active`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Active')`
The index of the currently active step.

`alternative_label`` ``=`` ``Boolean(default=False,`` ``label='Alternative`` ``label')`
Whether to place the step label below the step icon. Only applies to the
‘standard’ variant.

`back_text`` ``=`` ``String(default='Back',`` ``label='Back`` ``text')`
Label for the back navigation button. Only applies to the ‘compact’
variant.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the active and completed steps.

`connector`` ``=`` ``Boolean(default=True,`` ``label='Connector')`
Whether to display the connector line between steps. Only applies to the
‘standard’ variant.

`indicator`` ``=`` ``Selector(default='dots',`` ``label='Indicator',`` ``names={},`` ``objects=['dots',`` ``'progress',`` ``'text'])`
The type of progress indicator to display. Only applies to the ‘compact’
variant.

`next_text`` ``=`` ``String(default='Next',`` ``label='Next`` ``text')`
Label for the next navigation button. Only applies to the ‘compact’
variant.

`non_linear`` ``=`` ``Boolean(default=False,`` ``label='Non`` ``linear')`
Whether steps can be clicked to navigate non-linearly. Only applies to
the ‘standard’ variant.

`orientation`` ``=`` ``Selector(default='horizontal',`` ``label='Orientation',`` ``names={},`` ``objects=['horizontal',`` ``'vertical'])`
The orientation of the stepper. Use ‘vertical’ to stack the steps from
top to bottom (e.g. in a narrow sidebar). Only applies to the ‘standard’
variant.

`position`` ``=`` ``Selector(default='static',`` ``label='Position',`` ``names={},`` ``objects=['bottom',`` ``'static',`` ``'top'])`
The positioning of the bar. Only applies to the ‘compact’ variant.

`variant`` ``=`` ``Selector(default='standard',`` ``label='Variant',`` ``names={},`` ``objects=['standard',`` ``'compact'])`
The stepper variant. ‘standard’ renders a labelled horizontal strip;
‘compact’ renders a minimal mobile-style bar with an indicator and
navigation buttons.

back()
Return to the previous step.

next()
Advance to the next step.

reset()
Reset to the first step.

class panel.ui.widgets.Switch(\*, color, description_delay, edge, size, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget)

The Switch allows toggling a single condition between True/False states
by ticking a checkbox.

This widget is interchangeable with the Checkbox widget.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/Switch.html](https://panel-material-ui.holoviz.org/reference/widgets/Switch.html)

- [https://panel.holoviz.org/reference/widgets/Switch.html](https://panel.holoviz.org/reference/widgets/Switch.html)

- [https://mui.com/material-ui/react-switch/](https://mui.com/material-ui/react-switch/)

Example:

\>\>\> Switch(label='Works with the tools you know and love', value=True)\

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

`value`` ``=`` ``Boolean(default=False,`` ``label='Value')`
The widget value which the widget type resolves to when used as a
reactive param reference.

`width`` ``=`` ``Boolean(allow_None=True,`` ``allow_refs=True,`` ``label='Width')`
Width of the widget.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the switch.

`description_delay`` ``=`` ``Integer(default=1000,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Description`` ``delay')`
Delay (in milliseconds) to display the tooltip after the cursor has
hovered over the Button, default is 1000ms.

`edge`` ``=`` ``Selector(default=False,`` ``label='Edge',`` ``names={},`` ``objects=['start',`` ``'end',`` ``False])`
The edge position for the switch.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The size of the switch.

width = None

class panel.ui.widgets.TabMenu(\*, centered, color, icon_position, scroll_buttons, variant, active, items, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `MenuBase`

The TabMenu component is used to display a group of tabs that allow
users to switch between different views or sections of content. It
provides a clean, organized way to navigate between related items.

Tab items can be strings or objects with properties:

- label: The label of the tab item (required)

- icon: The icon of the tab item (optional)

- avatar: The avatar of the tab item (optional)

- href: Link to navigate to when clicking the tab item (optional)

- target: Link target (e.g. “\_blank”) (optional)

- tooltip: The tooltip text shown on hover (optional)

References:

- [https://panel-material-ui.holoviz.org/reference/menus/TabMenu.html](https://panel-material-ui.holoviz.org/reference/menus/TabMenu.html)

- [https://mui.com/material-ui/react-tabs/](https://mui.com/material-ui/react-tabs/)

Example:

\>\>\> pmui.TabMenu(items=\[\
...     {'label': 'Home', 'icon': 'home'},\
...     {'label': 'Gallery', 'icon': 'image'},\
...     {'label': 'Settings', 'icon': 'settings'},\
... \], active=0)\

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
> label, attached, description, disabled
>
> `panel_material_ui.widgets.menus.MenuBase`:
> value, margin, width, active, items
>
>

`centered`` ``=`` ``Boolean(default=False,`` ``label='Centered')`
Whether the tabs should be centered.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the tabs.

`icon_position`` ``=`` ``Selector(default='start',`` ``label='Icon`` ``position',`` ``names={},`` ``objects=['start',`` ``'top',`` ``'end',`` ``'bottom'])`
The position of the icon relative to the tab label.

`scroll_buttons`` ``=`` ``Selector(default='auto',`` ``label='Scroll`` ``buttons',`` ``names={},`` ``objects=['auto',`` ``'true',`` ``'false'])`
Determine behavior of scroll buttons when tabs are set to scroll. -
“auto” will only present them when not all the items are visible. -
“true” will always present them. - “false” will never present them.

`variant`` ``=`` ``Selector(default='standard',`` ``label='Variant',`` ``names={},`` ``objects=['standard',`` ``'scrollable',`` ``'fullWidth'])`
The variant to use for the tabs.

class panel.ui.widgets.Tabulator(value=None, **params)
Bases:
[BaseTable](panel.widgets.tables.md#panel.widgets.tables.BaseTable)

The Tabulator widget wraps the \[Tabulator
js\]([http://tabulator.info/](http://tabulator.info/)) table to provide
a full-featured, very powerful interactive table.

Reference:
[https://panel.holoviz.org/reference/widgets/Tabulator.html](https://panel.holoviz.org/reference/widgets/Tabulator.html)

Example:

\>\>\> Tabulator(df, theme='site', pagination='remote', page_size=25)\

Attributes:
[current_view](#panel.ui.widgets.Tabulator.current_view)
Returns the current view of the table after filtering and sorting are
applied.

Methods

|  |  |
|----|----|
| [download](#panel.ui.widgets.Tabulator.download)(\[filename\]) | Triggers downloading of the table as a CSV or JSON. |
| [download_menu](#panel.ui.widgets.Tabulator.download_menu)(\[text_kwargs, button_kwargs\]) | Returns a menu containing a TextInput and Button widget to set the filename and trigger a client-side download of the data. |
| [on_click](#panel.ui.widgets.Tabulator.on_click)(callback\[, column\]) | Register a callback to be executed when any cell is clicked. |
| [on_edit](#panel.ui.widgets.Tabulator.on_edit)(callback) | Register a callback to be executed when a cell is edited. |
| [stream](#panel.ui.widgets.Tabulator.stream)(stream_value\[, rollover, ...\]) | Streams (appends) the stream_value provided to the existing value in an efficient manner. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
> [class="reference internal" title="panel.widgets.tables.BaseTable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.tables.BaseTable](panel.widgets.tables.md#panel.widgets.tables.BaseTable):
> value, aggregators, editables, editors, formatters, hierarchical,
> show_index, sorters, text_align, titles, widths
>
>

`selection`` ``=`` ``_ListValidateWithCallable(allow_refs=True,`` ``bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'int'>,`` ``label='Selection')`
The currently selected rows of the table. It validates its values
against ‘selectable_rows’ if used.

`row_height`` ``=`` ``Integer(allow_refs=True,`` ``default=30,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Row`` ``height')`
The height of each table row.

`buttons`` ``=`` ``Dict(allow_refs=True,`` ``class_=<class`` ``'dict'>,`` ``default={},`` ``label='Buttons',`` ``nested_refs=True)`
Dictionary mapping from column name to a HTML element to use as the
button icon.

`container_popup`` ``=`` ``Boolean(allow_refs=True,`` ``default=True,`` ``label='Container`` ``popup')`
If True, popups will appear within the table container, otherwise popups
will be appended to the body element of the DOM.

`expanded`` ``=`` ``List(allow_refs=True,`` ``bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'int'>,`` ``label='Expanded',`` ``nested_refs=True)`
List of expanded rows, only applicable if a row_content function has
been defined.

`embed_content`` ``=`` ``Boolean(allow_refs=True,`` ``default=False,`` ``label='Embed`` ``content')`
Whether to embed the row_content or render it dynamically when a row is
expanded.

`filters`` ``=`` ``List(allow_refs=True,`` ``bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'dict'>,`` ``label='Filters')`
List of client-side filters declared as dictionaries containing ‘field’,
‘type’ and ‘value’ keys.

`frozen_columns`` ``=`` ``ClassSelector(allow_refs=True,`` ``class_=(<class`` ``'list'>,`` ``<class`` ``'dict'>),`` ``default=[],`` ``label='Frozen`` ``columns',`` ``nested_refs=True)`
One of: - List indicating the columns to freeze. The column(s) may be
selected by name or index. - Dict indicating columns to freeze as keys
and their freeze location as values, freeze location is either ‘right’
or ‘left’.

`frozen_rows`` ``=`` ``List(allow_refs=True,`` ``bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'int'>,`` ``label='Frozen`` ``rows',`` ``nested_refs=True)`
List indicating the rows to freeze. If set, the first N rows will be
frozen, which prevents them from scrolling out of frame; if set to a
negative value the last N rows will be frozen.

`groups`` ``=`` ``Dict(allow_refs=True,`` ``class_=<class`` ``'dict'>,`` ``default={},`` ``label='Groups',`` ``nested_refs=True)`
Dictionary mapping defining the groups.

`groupby`` ``=`` ``List(allow_refs=True,`` ``bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'str'>,`` ``label='Groupby',`` ``nested_refs=True)`
Groups rows in the table by one or more columns.

`header_align`` ``=`` ``ClassSelector(allow_refs=True,`` ``class_=(<class`` ``'dict'>,`` ``<class`` ``'str'>),`` ``default={},`` ``label='Header`` ``align',`` ``nested_refs=True)`
A mapping from column name to alignment or a fixed column alignment,
which should be one of ‘left’, ‘center’, ‘right’.

`header_filters`` ``=`` ``ClassSelector(allow_None=True,`` ``allow_refs=True,`` ``class_=(<class`` ``'bool'>,`` ``<class`` ``'dict'>),`` ``label='Header`` ``filters',`` ``nested_refs=True)`
Whether to enable filters in the header or dictionary configuring
filters for each column.

`header_tooltips`` ``=`` ``Dict(allow_refs=True,`` ``class_=<class`` ``'dict'>,`` ``default={},`` ``label='Header`` ``tooltips')`
Dictionary mapping from column name to a tooltip to show when hovering
over the column header.

`hidden_columns`` ``=`` ``List(allow_refs=True,`` ``bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'str'>,`` ``label='Hidden`` ``columns',`` ``nested_refs=True)`
List of columns to hide.

`movable_columns`` ``=`` ``Boolean(allow_refs=True,`` ``default=False,`` ``label='Movable`` ``columns')`
Whether columns can be reordered by dragging their headers.

`layout`` ``=`` ``Selector(allow_refs=True,`` ``default='fit_data_table',`` ``label='Layout',`` ``names={},`` ``objects=['fit_data',`` ``'fit_data_fill',`` ``'fit_data_stretch',`` ``'fit_data_table',`` ``'fit_columns'])`
Describes the column layout mode with one of the following options
‘fit_columns’, ‘fit_data’, ‘fit_data_stretch’, ‘fit_data_fill’,
‘fit_data_table’.

`initial_page_size`` ``=`` ``Integer(allow_refs=True,`` ``bounds=(1,`` ``None),`` ``default=20,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Initial`` ``page`` ``size')`
Initial page size if page_size is None and therefore automatically set.

`pagination`` ``=`` ``Selector(allow_None=True,`` ``allow_refs=True,`` ``label='Pagination',`` ``names={},`` ``objects=['local',`` ``'remote'])`
Defines the pagination mode of the Tabulator. - None No pagination is
applied, all rows are rendered. - ‘local’ (client-side) Pagination is
applied locally, i.e. the entire DataFrame is loaded and then
paginated. - ‘remote’ (server-side) Pagination is applied remotely, i.e.
only the current page is loaded from the server.

`page`` ``=`` ``Integer(allow_refs=True,`` ``default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Page')`
Currently selected page (indexed starting at 1), if pagination is
enabled.

`page_size`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(1,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Page`` ``size')`
Number of rows to render per page, if pagination is enabled.

`row_content`` ``=`` ``Callable(allow_None=True,`` ``label='Row`` ``content')`
A function which is given the DataFrame row and should return a Panel
object to render as additional detail below the row. The function may
also be asynchronous.

`selectable`` ``=`` ``ClassSelector(allow_refs=True,`` ``class_=(<class`` ``'bool'>,`` ``<class`` ``'str'>,`` ``<class`` ``'int'>),`` ``default=True,`` ``label='Selectable')`
Defines the selection mode of the Tabulator. - True Selects rows on
click. To select multiple use Ctrl-select, to select a range use
Shift-select - False Disables selection - ‘checkbox’ Adds a column of
checkboxes to toggle selections - ‘checkbox-single’ Same as ‘checkbox’
but header does not allow select/deselect all - ‘toggle’ Selection
toggles when clicked - int The maximum number of selectable rows.

`selectable_rows`` ``=`` ``Callable(allow_None=True,`` ``allow_refs=True,`` ``label='Selectable`` ``rows')`
A function which given a DataFrame should return a list of rows by
integer index, which are selectable.

`sortable`` ``=`` ``ClassSelector(allow_refs=True,`` ``class_=(<class`` ``'bool'>,`` ``<class`` ``'dict'>),`` ``default=True,`` ``label='Sortable')`
Whether the columns in the table should be sortable. Can either be
specified as a simple boolean toggling the behavior on and off or as a
dictionary specifying the option per column.

`theme`` ``=`` ``Selector(allow_refs=True,`` ``default='simple',`` ``label='Theme',`` ``names={},`` ``objects=['default',`` ``'site',`` ``'simple',`` ``'midnight',`` ``'modern',`` ``'bootstrap',`` ``'bootstrap4',`` ``'materialize',`` ``'bulma',`` ``'semantic-ui',`` ``'fast',`` ``'bootstrap5'])`
Tabulator CSS theme to apply to table.

`theme_classes`` ``=`` ``List(allow_refs=True,`` ``bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'str'>,`` ``label='Theme`` ``classes',`` ``nested_refs=True)`
List of extra CSS classes to apply to the Tabulator element to customize
the theme.

`title_formatters`` ``=`` ``Dict(allow_refs=True,`` ``class_=<class`` ``'dict'>,`` ``default={},`` ``label='Title`` ``formatters',`` ``nested_refs=True)`
Tabulator formatter specification to use for a particular column header
title.

property current_view: pd.DataFrame
Returns the current view of the table after filtering and sorting are
applied.

download(filename: str = 'table.csv')
Triggers downloading of the table as a CSV or JSON.

Parameters:
**filename: str**
The filename to save the table as.

download_menu(text_kwargs={}, button_kwargs={})
Returns a menu containing a TextInput and Button widget to set the
filename and trigger a client-side download of the data.

Parameters:
**text_kwargs: dict**
Keyword arguments passed to the TextInput constructor

**button_kwargs: dict**
Keyword arguments passed to the Button constructor

Returns:
filename: TextInput
The TextInput widget setting a filename.

button: Button
The Button that triggers a download.

on_click(callback: Callable\[\[CellClickEvent\], None\], column: str \| None = None)
Register a callback to be executed when any cell is clicked. The
callback is given a CellClickEvent declaring the column and row of the
cell that was clicked.

Parameters:
**callback: (callable)**
The callback to run on edit events.

**column: (str)**
Optional argument restricting the callback to a specific column.

on_edit(callback: Callable\[\[TableEditEvent\], None\])
Register a callback to be executed when a cell is edited. Whenever a
cell is edited on_edit callbacks are called with a TableEditEvent as the
first argument containing the column, row and value of the edited cell.

Parameters:
**callback: (callable)**
The callback to run on edit events.

stream(stream_value, rollover=None, reset_index=True, follow=True)
Streams (appends) the stream_value provided to the existing value in an
efficient manner.

Parameters:
**stream_value: (pd.DataFrame \| pd.Series \| Dict)**
The new value(s) to append to the existing value.

**rollover: int**
A maximum column size, above which data from the start of the column
begins to be discarded. If None, then columns will continue to grow
unbounded.

**reset_index: (bool, default=True)**
If True and the stream_value is a DataFrame, then its index is reset.
Helps to keep the index unique and named index

Raises:
ValueError: Raised if the stream_value is not a supported type.

Examples

Stream a Series to a DataFrame \>\>\> value = pd.DataFrame({“x”: \[1,
2\], “y”: \[“a”, “b”\]}) \>\>\> tabulator = Tabulator(value=value)
\>\>\> stream_value = pd.Series({“x”: 4, “y”: “d”}) \>\>\>
tabulator.stream(stream_value) \>\>\> tabulator.value.to_dict(“list”)
{‘x’: \[1, 2, 4\], ‘y’: \[‘a’, ‘b’, ‘d’\]}

Stream a Dataframe to a Dataframe \>\>\> value = pd.DataFrame({“x”: \[1,
2\], “y”: \[“a”, “b”\]}) \>\>\> tabulator = Tabulator(value=value)
\>\>\> stream_value = pd.DataFrame({“x”: \[3, 4\], “y”: \[“c”, “d”\]})
\>\>\> tabulator.stream(stream_value) \>\>\>
tabulator.value.to_dict(“list”) {‘x’: \[1, 2, 3, 4\], ‘y’: \[‘a’, ‘b’,
‘c’, ‘d’\]}

Stream a Dictionary row to a DataFrame \>\>\> value = pd.DataFrame({“x”:
\[1, 2\], “y”: \[“a”, “b”\]}) \>\>\> tabulator = Tabulator(value=value)
\>\>\> stream_value = {“x”: 4, “y”: “d”} \>\>\>
tabulator.stream(stream_value) \>\>\> tabulator.value.to_dict(“list”)
{‘x’: \[1, 2, 4\], ‘y’: \[‘a’, ‘b’, ‘d’\]}

Stream a Dictionary of Columns to a Dataframe \>\>\> value =
pd.DataFrame({“x”: \[1, 2\], “y”: \[“a”, “b”\]}) \>\>\> tabulator =
Tabulator(value=value) \>\>\> stream_value = {“x”: \[3, 4\], “y”: \[“c”,
“d”\]} \>\>\> tabulator.stream(stream_value) \>\>\>
tabulator.value.to_dict(“list”) {‘x’: \[1, 2, 3, 4\], ‘y’: \[‘a’, ‘b’,
‘c’, ‘d’\]}

class panel.ui.widgets.Terminal(output=None, **params)
Bases: [Widget](panel.widgets.base.md#panel.widgets.base.Widget)

The Terminal widget renders a live terminal in the browser using the
xterm.js library making it possible to display logs or even provide an
interactive terminal in a Panel application.

Reference:
[https://panel.holoviz.org/reference/widgets/Terminal.html](https://panel.holoviz.org/reference/widgets/Terminal.html)

Example:

\>\>\> Terminal(\
...     "Welcome to the Panel Terminal!", options={"cursorBlink": True}\
... )\

Attributes:
**clear**

**closed**

[subprocess](#panel.ui.widgets.Terminal.subprocess)
The subprocess enables running commands like ‘ls’, \[‘ls’, ‘-l’\],
‘bash’, ‘python’ and ‘ipython’ in the terminal.

Methods

|                |     |
|----------------|-----|
| **fileno**     |     |
| **flush**      |     |
| **getvalue**   |     |
| **read**       |     |
| **readable**   |     |
| **readlines**  |     |
| **seekable**   |     |
| **writable**   |     |
| **write**      |     |
| **writelines** |     |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
>

`value`` ``=`` ``String(constant=True,`` ``default='',`` ``readonly=True)`
User input received from the Terminal. Sent one character at the time.

`clear`` ``=`` ``Action(allow_None=True,`` ``constant=True,`` ``label='Clear')`
Clears the Terminal.

`options`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={},`` ``label='Options')`
Initial Options for the Terminal Constructor. cf. [https://xtermjs.org/docs/api/terminal/interfaces/iterminaloptions/](https://xtermjs.org/docs/api/terminal/interfaces/iterminaloptions/)

`output`` ``=`` ``String(default='',`` ``label='Output')`
System output written to the Terminal

`ncols`` ``=`` ``Integer(constant=True,`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Ncols',`` ``readonly=True)`
The number of columns in the terminal.

`nrows`` ``=`` ``Integer(constant=True,`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Nrows',`` ``readonly=True)`
The number of rows in the terminal.

`write_to_console`` ``=`` ``Boolean(default=False,`` ``label='Write`` ``to`` ``console')`
Whether or not to write to the server console.

`_clears`` ``=`` ``Integer(default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='`` ``clears')`
Sends a signal to clear the terminal

`_output`` ``=`` ``String(default='',`` ``label='`` ``output')`

property subprocess
The subprocess enables running commands like ‘ls’, \[‘ls’, ‘-l’\],
‘bash’, ‘python’ and ‘ipython’ in the terminal.

class panel.ui.widgets.TextAreaInput(\*, auto_grow, cols, enter_pressed, max_rows, resizable, rows, max_length, placeholder, size, color, error_state, helper_text, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_TextInputBase`

>
>
> The TextAreaInput allows entering any multiline string using a text
> input box.
>
> Lines are joined with the newline character \`
>
>

[\`](#id5).

>
>
> References:
>
> - href="https://panel-material-ui.holoviz.org/reference/widgets/TextAreaInput.html"
>   class="reference external">https://panel-material-ui.holoviz.org/reference/widgets/TextAreaInput.html
>
> - [class="reference external">https://panel.holoviz.org/reference/widgets/TextAreaInput.html](https://panel.holoviz.org/reference/widgets/TextAreaInput.html)
>
> - [class="reference external">https://mui.com/material-ui/react-text-field/](https://mui.com/material-ui/react-text-field/)
>
> Example:
>
>
>
>
>
> \>\>\> TextAreaInput(\
> ...     label='Description', placeholder='Enter your description here...'\
> ... )\
>
>
>
>
>
>

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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._TextInputBase`:
> value, max_length, placeholder, size, value_input
>
>

`auto_grow`` ``=`` ``Boolean(default=False,`` ``label='Auto`` ``grow')`
Whether the text area should automatically grow vertically to
accommodate the current text.

`cols`` ``=`` ``Integer(default=20,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Cols')`
Number of columns in the text input field.

`max_rows`` ``=`` ``Integer(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Max`` ``rows')`
When combined with auto_grow this determines the maximum number of rows
the input area can grow.

`rows`` ``=`` ``Integer(default=2,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Rows')`
Number of rows in the text input field.

`resizable`` ``=`` ``ObjectSelector(label='Resizable',`` ``names={},`` ``objects=['both',`` ``'width',`` ``'height',`` ``False])`
Whether the layout is interactively resizable, and if so in which
dimensions: width, height, or both. Can only be set during
initialization.

`enter_pressed`` ``=`` ``Event(default=False,`` ``label='Enter`` ``pressed')`
Event when Shift+Enter has been pressed.

class panel.ui.widgets.TextEditor(**params: Any)
Bases: [Widget](panel.widgets.base.md#panel.widgets.base.Widget)

The TextEditor widget provides a WYSIWYG (what-you-see-is-what-you-get)
rich text editor which outputs HTML.

The editor is built on top of the
\[Quill.js\]([https://quilljs.com/](https://quilljs.com/)) library.

Reference:
[https://panel.holoviz.org/reference/widgets/TextEditor.html](https://panel.holoviz.org/reference/widgets/TextEditor.html)

Example:

\>\>\> TextEditor(placeholder='Enter some text')\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width
>
>

`value`` ``=`` ``String(default='',`` ``label='Value')`
State of the current text in the editor if on_keyup. Otherwise, only
upon loss of focus, i.e. clicking outside the editor, or pressing
\<Ctrl+Enter\> or \<Cmd+Enter\>.

`disabled`` ``=`` ``Boolean(default=False,`` ``label='Disabled')`
Whether the editor is disabled.

`mode`` ``=`` ``Selector(default='toolbar',`` ``label='Mode',`` ``names={},`` ``objects=['bubble',`` ``'toolbar'])`
Whether to display a toolbar or a bubble menu on highlight.

`on_keyup`` ``=`` ``Boolean(default=True,`` ``label='On`` ``keyup')`
Whether to update the value on every key press or only upon loss of
focus / hotkeys.

`toolbar`` ``=`` ``ClassSelector(class_=(<class`` ``'list'>,`` ``<class`` ``'bool'>),`` ``default=True,`` ``label='Toolbar')`
Toolbar configuration either as a boolean toggle or a configuration
specified as a list.

`placeholder`` ``=`` ``String(default='',`` ``label='Placeholder')`
Placeholder output when the editor is empty.

`selection`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={},`` ``label='Selection')`
The current text selection in the editor, as
`{"text":`` ``"..."}`
when the user has a non-empty selection, else
`{}`. Updates live as the selection changes.

`value_input`` ``=`` ``String(default='',`` ``label='Value`` ``input')`
State of the current text updated on every key press. Identical to value
if on_keyup.

class panel.ui.widgets.TextInput(\*, enter_pressed, max_length, placeholder, size, color, error_state, helper_text, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_TextInputBase`

The TextInput widget allows entering any string using a text input box.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/TextInput.html](https://panel-material-ui.holoviz.org/reference/widgets/TextInput.html)

- [https://panel.holoviz.org/reference/widgets/TextInput.html](https://panel.holoviz.org/reference/widgets/TextInput.html)

- [https://mui.com/material-ui/react-text-field/](https://mui.com/material-ui/react-text-field/)

Example:

\>\>\> TextInput(label='Name', placeholder='Enter your name here ...')\

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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._TextInputBase`:
> value, max_length, placeholder, size, value_input
>
>

`enter_pressed`` ``=`` ``Event(default=False,`` ``label='Enter`` ``pressed')`
Event when the enter key has been pressed.

class panel.ui.widgets.TextToSpeech(\*, \_voices, auto_speak, cancel, pause, resume, speak, lang, pitch, rate, voice, volume, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: [Utterance](panel.widgets.text_to_speech.md#panel.widgets.text_to_speech.Utterance),
[Widget](panel.widgets.base.md#panel.widgets.base.Widget)

The TextToSpeech widget wraps the HTML5 SpeechSynthesis API

See [https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis)

Reference:
[https://panel.holoviz.org/reference/widgets/TextToSpeech.html](https://panel.holoviz.org/reference/widgets/TextToSpeech.html)

Example:

\>\>\> TextToSpeech(label="Speech Synthesis", value="Data apps are nice")\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
> href="panel.widgets.text_to_speech.html#panel.widgets.text_to_speech.Utterance"
> class="reference internal"
> title="panel.widgets.text_to_speech.Utterance"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.text_to_speech.Utterance:
> value, lang, pitch, rate, voice, volume
>
>

`auto_speak`` ``=`` ``Boolean(default=True,`` ``label='Auto`` ``speak')`
Whether or not to automatically speak when the value changes.

`cancel`` ``=`` ``Event(default=False,`` ``label='Cancel')`
Removes all utterances from the utterance queue.

`pause`` ``=`` ``Event(default=False,`` ``label='Pause')`
Puts the TextToSpeak object into a paused state.

`resume`` ``=`` ``Event(default=False,`` ``label='Resume')`
Puts the TextToSpeak object into a non-paused state: resumes it if it
was already paused.

`paused`` ``=`` ``Boolean(constant=True,`` ``default=False,`` ``label='Paused',`` ``readonly=True)`
A Boolean that returns true if the TextToSpeak object is in a paused
state.

`pending`` ``=`` ``Boolean(constant=True,`` ``default=False,`` ``label='Pending',`` ``readonly=True)`
A Boolean that returns true if the utterance queue contains
as-yet-unspoken utterances.

`speak`` ``=`` ``Event(default=False,`` ``label='Speak')`
Speak. I.e. send a new Utterance to the browser

`speaking`` ``=`` ``Boolean(constant=True,`` ``default=False,`` ``label='Speaking',`` ``readonly=True)`
A Boolean that returns true if an utterance is currently in the process
of being spoken — even if TextToSpeak is in a paused state.

`voices`` ``=`` ``List(bounds=(0,`` ``None),`` ``constant=True,`` ``default=[],`` ``item_type=<class`` ``'panel.widgets.text_to_speech.Voice'>,`` ``label='Voices',`` ``readonly=True)`
Returns a list of Voice objects representing all the available voices on
the current device.

`_voices`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'panel.widgets.text_to_speech.Voice'>,`` ``label='`` ``voices')`

class panel.ui.widgets.TimePicker(\*, color, end, error_state, format, helper_text, mode, size, start, variant, clock, hour_increment, minute_increment, second_increment, seconds, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_TimeCommon`

The TimePicker allows selecting a time value using a text box and a
time-picking utility.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/TimePicker.html](https://panel-material-ui.holoviz.org/reference/widgets/TimePicker.html)

- [https://panel.holoviz.org/reference/widgets/TimePicker.html](https://panel.holoviz.org/reference/widgets/TimePicker.html)

- [https://mui.com/x/react-date-pickers/time-picker/](https://mui.com/x/react-date-pickers/time-picker/)

Example:

\>\>\> TimePicker(\
...     value=time(12, 59, 31), start="09:00:00", end="18:00:00", label="Time"\
... )\

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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.input._TimeCommon`:
> clock, hour_increment, minute_increment, second_increment, seconds
>
>

`value`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'datetime.time'>,`` ``<class`` ``'str'>),`` ``label='Value')`
The current value

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the time picker.

`error_state`` ``=`` ``Boolean(default=False,`` ``label='Error`` ``state')`
Whether to display in error state.

`helper_text`` ``=`` ``String(default='',`` ``label='Helper`` ``text')`
Helper text displayed below the input field.

`start`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'datetime.time'>,`` ``<class`` ``'str'>),`` ``label='Start')`
Inclusive lower bound of the allowed time selection

`end`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'datetime.time'>,`` ``<class`` ``'str'>),`` ``label='End')`
Inclusive upper bound of the allowed time selection

`format`` ``=`` ``String(allow_None=True,`` ``label='Format')`
Format to display the time. Use ‘HH:mm:ss’ to include seconds. For
12-hour clock, use ‘hh:mm a’. See dayjs formatting options. If None,
will be automatically set based on clock and seconds settings.
+—-+————————————+————+ \| H \| Hours \| 0 to 23 \| \| HH \| Hours,
2-digits \| 00 to 23 \| \| h \| Hours, 12-hour clock \| 1 to 12 \| \| hh
\| Hours, 12-hour clock, 2-digits \| 1 to 12 \| \| m \| Minutes \| 0 to
59 \| \| mm \| Minutes \| 00 to 59 \| \| s \| Seconds \| 0, 1 to 59 \|
\| ss \| Seconds \| 00 to 59 \| \| a \| am/pm, lower-case \| am or pm \|
\| A \| AM/PM, upper-cas \| AM or PM \| +—-+————————————+————+

`mode`` ``=`` ``Selector(default='auto',`` ``label='Mode',`` ``names={},`` ``objects=['digital',`` ``'analog',`` ``'auto'])`
Whether to render a digital or analog clock. By default automatically
switches between digital clock on desktop to analog clock on mobile.

`size`` ``=`` ``Selector(default='medium',`` ``label='Size',`` ``names={},`` ``objects=['small',`` ``'medium',`` ``'large'])`
The visual size of the time picker input.

`variant`` ``=`` ``Selector(default='outlined',`` ``label='Variant',`` ``names={},`` ``objects=['filled',`` ``'outlined',`` ``'standard'])`
The variant style of the time picker.

class panel.ui.widgets.Toggle(\*, clicks, disable_elevation, end_icon, icon, icon_size, size, description_delay, attached, description, dark_theme, sx, theme_config, use_shadow_dom, button_style, button_type, color, variant, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_ButtonBase`

The Toggle widget allows toggling a single condition between True/False
states.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/Toggle.html](https://panel-material-ui.holoviz.org/reference/widgets/Toggle.html)

- [https://panel.holoviz.org/reference/widgets/Toggle.html](https://panel.holoviz.org/reference/widgets/Toggle.html)

- [https://mui.com/material-ui/react-toggle-button/](https://mui.com/material-ui/react-toggle-button/)

Example:

\>\>\> Toggle(label='Enable feature')\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
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
> label, margin, attached, disabled
>
> `panel_material_ui.widgets.button._ButtonLike`:
> description, button_style, button_type, color, description_delay
>
> `panel_material_ui.widgets.button._ButtonBase`:
> width, variant, clicks, disable_elevation, end_icon, icon, size
>
>

`value`` ``=`` ``Boolean(default=False,`` ``label='Value')`
The widget value which the widget type resolves to when used as a
reactive param reference.

`icon_size`` ``=`` ``String(default='1.8em',`` ``label='Icon`` ``size')`
Size of the icon as a string, e.g. 12px or 1em.

class panel.ui.widgets.ToggleGroup(\*, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases:
[ToggleGroup](panel.widgets.select.md#panel.widgets.select.ToggleGroup)

A factory of Material toggle groups, a group of widgets which can be
switched on or off.

The widget_type selects between ‘button’ (default) and ‘box’ widgets and
the behavior between ‘check’ (default), where any number of options may
be selected and the value is a list, and ‘radio’, where exactly one
option is selected.

References:

- [https://panel.holoviz.org/reference/widgets/ToggleGroup.html](https://panel.holoviz.org/reference/widgets/ToggleGroup.html)

Example:

\>\>\> ToggleGroup(\
...     label='Fruits', options=\['Apple', 'Banana', 'Pear'\], behavior='radio'\
... )\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
> [class="reference internal" title="panel.widgets.select.SelectBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SelectBase](panel.widgets.select.md#panel.widgets.select.SelectBase):
> options
>
> href="panel.widgets.select.html#panel.widgets.select.SingleSelectBase"
> class="reference internal"
> title="panel.widgets.select.SingleSelectBase"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.select.SingleSelectBase:
> value
>
>

class panel.ui.widgets.ToggleIcon(\*, color, description_delay, active_icon, icon, icon_size, size, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `_ClickableIcon`

The ToggleIcon widget allows toggling a single condition between
True/False states. This widget is interchangeable with the Checkbox and
Switch widget.

This widget incorporates a value attribute, which alternates between
False and True.

References:

- [https://panel-material-ui.holoviz.org/reference/widgets/ToggleIcon.html](https://panel-material-ui.holoviz.org/reference/widgets/ToggleIcon.html)

- [https://panel.holoviz.org/reference/widgets/ToggleIcon.html](https://panel.holoviz.org/reference/widgets/ToggleIcon.html)

- [https://mui.com/material-ui/react-checkbox/#icon](https://mui.com/material-ui/react-checkbox/#icon)

Example:

\>\>\> ToggleIcon(\
...     icon="thumb-up", active_icon="thumb-down", size="small", description="Like"\
... )\

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
> `panel_material_ui.widgets.icon._ClickableIcon`:
> value, active_icon, icon, icon_size, size
>
>

`width`` ``=`` ``Boolean(allow_None=True,`` ``allow_refs=True,`` ``label='Width')`
Width of the widget.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the icon.

`description_delay`` ``=`` ``Integer(default=1000,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Description`` ``delay')`
Delay (in milliseconds) to display the tooltip after the cursor has
hovered over the Button, default is 1000ms.

width = None

class panel.ui.widgets.TooltipIcon(**params: Any)
Bases: [Widget](panel.widgets.base.md#panel.widgets.base.Widget)

The TooltipIcon displays a small ? icon. When you hover over the ? icon,
the value will display.

Use the TooltipIcon to provide

- helpful information to users without taking up a lot of screen space

- tooltips next to Panel widgets that do not support tooltips yet.

Reference: [https://panel.holoviz.org/reference/indicators/TooltipIcon.html](https://panel.holoviz.org/reference/indicators/TooltipIcon.html)

Example:

\>\>\> pn.widgets.TooltipIcon(value="This is a simple tooltip by using a string")\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> aspect_ratio, css_classes, design, min_width, min_height, max_width,
> max_height, styles, stylesheets, tags, width_policy, height_policy,
> sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
>

`value`` ``=`` ``ClassSelector(class_=(<class`` ``'str'>,`` ``<class`` ``'bokeh.models.ui.tooltips.Tooltip'>),`` ``default='Description',`` ``label='Value')`
The description in the tooltip.

`align`` ``=`` ``Align(default='center',`` ``label='Align')`
Whether the object should be aligned with the start, end or center of
its container. If set as a tuple it will declare (vertical, horizontal)
alignment.

class panel.ui.widgets.Tqdm(\*, layout, lock, max, progress, text, text_pane, write_to_console, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases:
[Tqdm](panel.widgets.indicators.md#panel.widgets.indicators.Tqdm)

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, disabled
>
> `panel.widgets.indicators.Indicator`:
> sizing_mode
>
> [class="reference internal" title="panel.widgets.indicators.Tqdm"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.indicators.Tqdm](panel.widgets.indicators.md#panel.widgets.indicators.Tqdm):
> value, margin, width, layout, lock, max, progress, text, text_pane,
> write_to_console
>
>

class panel.ui.widgets.Tree(\*, checkboxes, color, multi_select, propagate_to_child, propagate_to_parent, expanded, level_indent, show_children, active, items, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `TreeLikeBase`

The Tree component displays hierarchical data using a Material UI
RichTreeView, with optional checkboxes and multi-selection.

Items follow the same convention as MenuList:

Each item is a dictionary with at least:

>
>
> - `label` (str): Display label of the node.
>
>

The `id` field is optional. When omitted, a
stable internal id is generated from the item’s position, so the
simplest
`{"label":`` ``"Node"}`
form works without any additional bookkeeping.

Optional item fields:

>
>
> - `items` (list): Nested children, each with
>   the same schema.
>
> - `icon` (str): MUI icon name (rendered via
>   `<Icon>`).
>
> - `file_type` (str): Helper for common icons,
>   one of `"image"`,
>   `"pdf"`, `"doc"`,
>   `"video"`,
>   `"folder"`,
>   `"pinned"`,
>   `"trash"`.
>
> - `disabled` (bool): Whether the item is
>   disabled.
>
> - `selectable` (bool): Whether the item is
>   selectable.
>
> - `secondary` (str): The secondary text of
>   the item.
>
> - `actions` (list): Actions to display on the
>   item.
>
> - `buttons` (list): Buttons to display on the
>   item.
>
> - `color` (str): The color of the item.
>
> - `tooltip` (str): The tooltip text shown on
>   hover.
>
>

Example:

\>\>\> pmui.Tree(\
...     items=\[\
...         {\
...             "id": "documents",\
...             "label": "Documents",\
...             "file_type": "folder",\
...             "items": \[\
...                 {\
...                     "id": "invoice",\
...                     "label": "Invoice Q1.pdf",\
...                     "file_type": "pdf",\
...                 },\
...                 {\
...                     "id": "notes",\
...                     "label": "Meeting notes.docx",\
...                     "file_type": "doc",\
...                 },\
...             \],\
...         },\
...         {\
...             "id": "trash",\
...             "label": "Trash",\
...             "file_type": "trash",\
...         },\
...     \],\
...     active=\[(0,)\],\
... )\

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
> label, attached, description, disabled
>
> `panel_material_ui.widgets.menus.MenuBase`:
> margin, width, items
>
> `panel_material_ui.widgets.menus.TreeLikeBase`:
> expanded, level_indent, show_children
>
>

`value`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'dict'>,`` ``label='Value')`
The list of currently selected item dictionaries. This parameter is
synchronized with the active parameter and reflects the items that are
currently selected in the tree. Each item is represented as a dictionary
containing its properties (e.g., ‘id’, ‘label’, etc.).

`active`` ``=`` ``List(allow_None=True,`` ``item_type=<class`` ``'tuple'>,`` ``label='Active')`
The index(es) of currently selected items. Provide a list of tuples of
indices, e.g.
`[(0,`` ``1)]` to
refer to the second child beneath the first root node.

`checkboxes`` ``=`` ``Boolean(default=False,`` ``label='Checkboxes')`
Whether to show selection checkboxes next to each tree item.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
Color palette key for the selected node styling.

`multi_select`` ``=`` ``Boolean(default=True,`` ``label='Multi`` ``select')`
Whether multiple tree items can be selected at once.

`propagate_to_parent`` ``=`` ``Boolean(default=False,`` ``label='Propagate`` ``to`` ``parent')`
Whether checkbox selection propagates from child nodes to parent nodes.
If True, selecting a child will also select its parent(s).

`propagate_to_child`` ``=`` ``Boolean(default=False,`` ``label='Propagate`` ``to`` ``child')`
Whether checkbox selection propagates from parent nodes to child nodes.
If True, selecting a parent node will automatically select all its child
nodes. If False, selection is independent for each node.

class panel.ui.widgets.Trend(\*, data, layout, neg_color, plot_color, plot_type, plot_x, plot_y, pos_color, value_change, selection, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases: `SyncableData`,
`Indicator`

The Trend indicator enables the user to display a dashboard kpi card.

The card can be layout out as:

- a column (text and plot on top of each other) or a row (text and

- plot after each other)

Reference:
[https://panel.holoviz.org/reference/indicators/Trend.html](https://panel.holoviz.org/reference/indicators/Trend.html)

Example:

\>\>\> data = {'x': np.arange(50), 'y': np.random.randn(50).cumsum()}\
\>\>\> Trend(label='Price', data=data, plot_type='area', width=200, height=200)\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
> `panel.reactive.SyncableData`: selection
>
>

`label`` ``=`` ``String(default='',`` ``label='Label')`
The label or a short description of the card.

`value`` ``=`` ``Parameter(default='auto',`` ``label='Value')`
The primary value to be displayed.

`sizing_mode`` ``=`` ``Selector(label='Sizing`` ``mode',`` ``names={},`` ``objects=['fixed',`` ``'stretch_width',`` ``'stretch_height',`` ``'stretch_both',`` ``'scale_width',`` ``'scale_height',`` ``'scale_both',`` ``None])`
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

`data`` ``=`` ``Parameter(allow_None=True,`` ``label='Data')`
The plot data declared as a dictionary of arrays or a DataFrame.

`layout`` ``=`` ``Selector(default='column',`` ``label='Layout',`` ``names={},`` ``objects=['column',`` ``'row'])`
The layout of the indicator, either a column (text and plot on top of
each other) or a row (text and plot after each other).

`plot_x`` ``=`` ``String(default='x',`` ``label='Plot`` ``x')`
The name of the key in the plot_data to use on the x-axis.

`plot_y`` ``=`` ``String(default='y',`` ``label='Plot`` ``y')`
The name of the key in the plot_data to use on the y-axis.

`plot_color`` ``=`` ``String(default='#428bca',`` ``label='Plot`` ``color')`
The color to use in the plot.

`plot_type`` ``=`` ``Selector(default='bar',`` ``label='Plot`` ``type',`` ``names={},`` ``objects=['line',`` ``'step',`` ``'area',`` ``'bar'])`
The plot type to render the plot data as.

`pos_color`` ``=`` ``String(default='#5cb85c',`` ``label='Pos`` ``color')`
The color used to indicate a positive change.

`neg_color`` ``=`` ``String(default='#d9534f',`` ``label='Neg`` ``color')`
The color used to indicate a negative change.

`value_change`` ``=`` ``Parameter(default='auto',`` ``label='Value`` ``change')`
A secondary value. For example the change in percent.

sizing_mode: t.Literal\['fixed', 'stretch_width', 'stretch_height', 'stretch_both', 'scale_width', 'scale_height', 'scale_both'\] \| None = None

class panel.ui.widgets.TupleInput(\*, enter_pressed, max_length, size, color, error_state, helper_text, variant, attached, dark_theme, sx, theme_config, use_shadow_dom, description, placeholder, serializer, type, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases:
[LiteralInput](#panel.ui.widgets.LiteralInput)

The TupleInput allows entering a tuple value using a text input box.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height
>
> [class="reference internal"
> title="panel.widgets.input.LiteralInput"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets. input .LiteralInput](panel.widgets.input.md#panel.widgets.input.LiteralInput):
> serializer
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
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._TextInputBase`:
> max_length, placeholder, size
>
> [title="panel_material_ui.widgets.input.TextInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets. input .TextInput](#panel.ui.widgets.TextInput):
> enter_pressed
>
> [title="panel_material_ui.widgets.input.LiteralInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets. input .LiteralInput](#panel.ui.widgets.LiteralInput):
> value_input
>
>

`value`` ``=`` ``Parameter(default=(),`` ``label='Value')`
The widget value which the widget type resolves to when used as a
reactive param reference.

`type`` ``=`` ``ClassSelector(class_=<class`` ``'type'>,`` ``constant=True,`` ``default=<class`` ``'tuple'>,`` ``label='Type',`` ``readonly=True)`
The type of the value.

type
alias of `tuple`

class panel.ui.widgets.Utterance(\*, lang, pitch, rate, value, voice, volume, name)
Bases: `Parameterized`

An *utterance* is the smallest unit of speech in spoken language
analysis.

The Utterance Model wraps the HTML5 SpeechSynthesisUtterance API

See [https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisUtterance](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisUtterance)

Methods

|  |  |
|----|----|
| [set_voices](#panel.ui.widgets.Utterance.set_voices)(voices) | Updates the lang and voice parameter objects, default and value |
| [to_dict](#panel.ui.widgets.Utterance.to_dict)(\[include_uuid\]) | Returns the object parameter values in a dictionary |

**Parameter Definitions**

------------------------------------------------------------------------

`value`` ``=`` ``String(default='',`` ``label='Value')`
The text that will be synthesised when the utterance is spoken. The text
may be provided as plain text, or a well-formed SSML document.

`lang`` ``=`` ``Selector(default='',`` ``label='Lang',`` ``names={},`` ``objects=[''])`
The language of the utterance.

`pitch`` ``=`` ``Number(bounds=(0.0,`` ``2.0),`` ``default=1.0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Pitch')`
The pitch at which the utterance will be spoken at expressed as a number
between 0 and 2.

`rate`` ``=`` ``Number(bounds=(0.1,`` ``10.0),`` ``default=1.0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Rate')`
The speed at which the utterance will be spoken at expressed as a number
between 0.1 and 10.

`voice`` ``=`` ``Selector(label='Voice',`` ``names={},`` ``objects=[])`
The voice that will be used to speak the utterance.

`volume`` ``=`` ``Number(bounds=(0.0,`` ``1.0),`` ``default=1.0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Volume')`
The volume that the utterance will be spoken at expressed as a number
between 0 and 1.

set_voices(voices)
Updates the lang and voice parameter objects, default and value

to_dict(include_uuid=True)
Returns the object parameter values in a dictionary

Returns:
Dict: \[description\]

class panel.ui.widgets.VideoStream(**params: Any)
Bases: [Widget](panel.widgets.base.md#panel.widgets.base.Widget)

The VideoStream displays a video from a local stream (for example from a
webcam) and allows accessing the streamed video data from Python.

Reference:
[https://panel.holoviz.org/reference/widgets/VideoStream.html](https://panel.holoviz.org/reference/widgets/VideoStream.html)

Example:

\>\>\> VideoStream(label='Video Stream', timeout=100)\

Methods

|  |  |
|----|----|
| [snapshot](#panel.ui.widgets.VideoStream.snapshot)() | Triggers a snapshot of the current VideoStream state to sync the widget value. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width, disabled
>
>

`value`` ``=`` ``String(default='',`` ``label='Value')`
A base64 representation of the video stream snapshot.

`format`` ``=`` ``Selector(default='png',`` ``label='Format',`` ``names={},`` ``objects=['png',`` ``'jpeg'])`
The file format as which the video is returned.

`paused`` ``=`` ``Boolean(default=False,`` ``label='Paused')`
Whether the video is currently paused

`timeout`` ``=`` ``Number(allow_None=True,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Timeout')`
Interval between snapshots in millisecons

snapshot()
Triggers a snapshot of the current VideoStream state to sync the widget
value.

class panel.ui.widgets.Voice(\*, default, lang, local_service, voice_uri, name)
Bases: `Parameterized`

The current device (i.e. OS and Browser) provides a list of Voices. Each
with a unique name and speaking a specific language.

Wraps the HTML5 SpeecSynthesisVoice API

See [https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisVoice](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisVoice)

Methods

|  |  |
|----|----|
| [group_by_lang](#panel.ui.widgets.Voice.group_by_lang)(voices) | Returns a dictionary where the key is the lang and the value is a list of voices for that language. |
| [to_voices_list](#panel.ui.widgets.Voice.to_voices_list)(voices) | Returns a list of Voice objects from the list of dicts provided |

**Parameter Definitions**

------------------------------------------------------------------------

`default`` ``=`` ``Boolean(constant=True,`` ``default=False,`` ``label='Default')`
A Boolean indicating whether the voice is the default voice for the
current app language (True), or not (False.)

`lang`` ``=`` ``String(constant=True,`` ``default='',`` ``label='Lang')`
Returns a BCP 47 language tag indicating the language of the voice.

`local_service`` ``=`` ``Boolean(constant=True,`` ``default=False,`` ``label='Local`` ``service')`
A Boolean indicating whether the voice is supplied by a local speech
synthesizer service (True), or a remote speech synthesizer service
(False.)

`voice_uri`` ``=`` ``String(constant=True,`` ``default='',`` ``label='Voice`` ``uri')`
Returns the type of URI and location of the speech synthesis service for
this voice.

static group_by_lang(voices)
Returns a dictionary where the key is the lang and the value is a list
of voices for that language.

static to_voices_list(voices)
Returns a list of Voice objects from the list of dicts provided

class panel.ui.widgets.Widget(**params: Any)
Bases: [Reactive](panel.reactive.md#panel.reactive.Reactive),
[WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase)

Widgets allow syncing changes in bokeh widget models with the parameters
on the Widget instance.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label, value
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, min_width, min_height,
> max_width, max_height, styles, stylesheets, tags, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
>

`height`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Height')`
The height of the component (in pixels). This can be either fixed or
preferred height, depending on height sizing policy.

`margin`` ``=`` ``Margin(allow_None=True,`` ``allow_refs=True,`` ``default=(5,`` ``10),`` ``label='Margin')`
Allows to create additional space around the component. May be specified
as a two-tuple of the form (vertical, horizontal) or a four-tuple (top,
right, bottom, left).

`width`` ``=`` ``Integer(allow_None=True,`` ``allow_refs=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Width')`
The width of the component (in pixels). This can be either fixed or
preferred width, depending on width sizing policy.

`disabled`` ``=`` ``Boolean(allow_refs=True,`` ``default=False,`` ``label='Disabled')`
Whether the widget is disabled.

class panel.ui.widgets.WidgetBase(**params: Any)
Bases: `Parameterized`

WidgetBase provides an abstract baseclass for widget components which
can be used to implement a custom widget-like type without implementing
the methods associated with a Reactive Panel component, e.g. it may be
used as a mix-in to a PyComponent or JSComponent.

Attributes:
**rx**

Methods

|  |  |
|----|----|
| [from_param](#panel.ui.widgets.WidgetBase.from_param)(parameter, **params) | Construct a widget from a Parameter and link the two bi-directionally. |
| [from_values](#panel.ui.widgets.WidgetBase.from_values)(values, **params) | Creates an instance of this Widget where the parameters are inferred from the data. |

**Parameter Definitions**

------------------------------------------------------------------------

`label`` ``=`` ``String(allow_refs=True,`` ``default='',`` ``label='Label')`
The label for the widget.

`value`` ``=`` ``Parameter(allow_None=True,`` ``label='Value')`
The widget value which the widget type resolves to when used as a
reactive param reference.

classmethod from_param(parameter: param.Parameter, **params) → T
Construct a widget from a Parameter and link the two bi-directionally.

Parameters:
**parameter: param.Parameter**
A parameter to create the widget from.

Returns:
Widget instance linked to the supplied parameter

classmethod from_values(values, **params)
Creates an instance of this Widget where the parameters are inferred
from the data.

Parameters:
**values: Iterable**
The values to infer the parameters from.

**params: dict**
Additional parameters to pass to the widget.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
