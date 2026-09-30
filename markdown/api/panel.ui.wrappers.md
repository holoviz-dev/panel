# panel.ui.wrappers package

## Module contents

Components that wrap another component, e.g. to add a badge or a
tooltip.

class panel.ui.wrappers.Badge(object=None, **params)
Bases: [Wrapper](#panel.ui.wrappers.Wrapper)

The Badge generates a small badge to the top-right (by default) of its
child element. Badges are commonly used to display notification counts,
status indicators, or short labels overlaid on icons, avatars, or
buttons.

References:

- [https://panel-material-ui.holoviz.org/reference/wrappers/Badge.html](https://panel-material-ui.holoviz.org/reference/wrappers/Badge.html)

- [https://mui.com/material-ui/react-badge/](https://mui.com/material-ui/react-badge/)

Example:

\>\>\> Badge(IconButton(icon="mail"), content=4, color="primary")\

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
> [title="panel_material_ui.wrappers.base.Wrapper"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.wrappers.base.Wrapper](#panel.ui.wrappers.Wrapper):
> object
>
>

`content`` ``=`` ``Parameter(default=0,`` ``label='Content')`
The content rendered within the badge. Typically an integer count but
can be a short string.

`color`` ``=`` ``Selector(default='primary',`` ``label='Color',`` ``names={},`` ``objects=['default',`` ``'primary',`` ``'secondary',`` ``'error',`` ``'info',`` ``'success',`` ``'warning',`` ``'light',`` ``'dark',`` ``'danger'])`
The color of the badge.

`max`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=99,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Max')`
Maximum count to display. Values above this show as ‘max+’ (e.g. ‘99+’).

`offset`` ``=`` ``XYCoordinates(allow_None=True,`` ``label='Offset',`` ``length=2)`
The (x, y) pixel offset of the badge from its anchor point on the
object. Positive x shifts the badge right, positive y down.

`overlap`` ``=`` ``Selector(default='rectangular',`` ``label='Overlap',`` ``names={},`` ``objects=['rectangular',`` ``'circular'])`
Wrapped shape the badge should overlap.

`placement`` ``=`` ``Selector(default='top-right',`` ``label='Placement',`` ``names={},`` ``objects=['top-right',`` ``'top-left',`` ``'bottom-right',`` ``'bottom-left'])`
The placement of the badge relative to the child element.

`show_zero`` ``=`` ``Boolean(default=False,`` ``label='Show`` ``zero')`
Whether to display the badge when content is zero.

`variant`` ``=`` ``Selector(default='standard',`` ``label='Variant',`` ``names={},`` ``objects=['dot',`` ``'standard'])`
The variant of the badge. Use ‘dot’ for a small dot indicator without
content.

class panel.ui.wrappers.Clickable(object=None, **params)
Bases: [Wrapper](#panel.ui.wrappers.Wrapper),
`_ClickButton`

The Clickable wrapper adds click interaction to any child component. It
wraps a single child element with a clickable area, providing a clicks
counter and an on_click callback mechanism.

Optionally renders a Material UI ripple effect on click.

References:

- [https://mui.com/material-ui/api/button-base/](https://mui.com/material-ui/api/button-base/)

Example:

\>\>\> Clickable(Card(...), on_click=lambda e: print("Clicked!"))\

Methods

|  |  |
|----|----|
| [on_click](#panel.ui.wrappers.Clickable.on_click)(callback) | Register a callback to be executed when the component is clicked. |

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
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, margin, width
>
> [class="reference internal" title="panel.custom.ReactComponent"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.custom.ReactComponent](panel.custom.md#panel.custom.ReactComponent):
> use_shadow_dom
>
> [class="reference internal"
> title="panel_material_ui.base.MaterialComponent"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.base.MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent):
> loading, dark_theme, theme_config, sx
>
> [title="panel_material_ui.wrappers.base.Wrapper"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.wrappers.base.Wrapper](#panel.ui.wrappers.Wrapper):
> object
>
>

`value`` ``=`` ``Event(default=False,`` ``label='Value')`
Toggles from False to True while the event is being processed.

`disabled`` ``=`` ``Boolean(allow_refs=True,`` ``default=False,`` ``label='Disabled')`
Whether the clickable area is disabled.

`clicks`` ``=`` ``Integer(default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Clicks')`
Number of clicks. Increment triggers registered callbacks.

`disable_ripple`` ``=`` ``Boolean(default=False,`` ``label='Disable`` ``ripple')`
Whether to disable the ripple effect on click.

on_click(callback: Callable\[\[Event\], None \| Awaitable\[None\]\]) → Watcher
Register a callback to be executed when the component is clicked.

Returns:
watcher: param.Parameterized.Watcher
A Watcher that executes the callback when clicked.

class panel.ui.wrappers.Skeleton(object=None, **params)
Bases: [Wrapper](#panel.ui.wrappers.Wrapper)

The Skeleton wraps a child component and displays an animated
placeholder in its place while loading. When active is True the skeleton
is shown; when False the child is rendered normally.

References:

- [https://panel-material-ui.holoviz.org/reference/wrappers/Skeleton.html](https://panel-material-ui.holoviz.org/reference/wrappers/Skeleton.html)

- [https://mui.com/material-ui/react-skeleton/](https://mui.com/material-ui/react-skeleton/)

Example:

\>\>\> Skeleton(Card(...), active=True, variant="rounded")\

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
> [title="panel_material_ui.wrappers.base.Wrapper"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.wrappers.base.Wrapper](#panel.ui.wrappers.Wrapper):
> object
>
>

`active`` ``=`` ``Boolean(default=False,`` ``label='Active')`
Whether to show the child content. When False the skeleton placeholder
is rendered; when True the child is displayed normally.

`animation`` ``=`` ``Selector(default='pulse',`` ``label='Animation',`` ``names={},`` ``objects=['pulse',`` ``'wave',`` ``None])`
The animation effect for the skeleton. Use None to disable.

`variant`` ``=`` ``Selector(default='rounded',`` ``label='Variant',`` ``names={},`` ``objects=['text',`` ``'circular',`` ``'rectangular',`` ``'rounded'])`
Shape variant of the skeleton placeholder.

class panel.ui.wrappers.Tooltip(object=None, **params)
Bases: [Wrapper](#panel.ui.wrappers.Wrapper)

The Tooltip displays informative text when users hover over, focus on,
or tap a child element. It wraps a single child component and shows a
configurable tooltip label.

References:

- [https://panel-material-ui.holoviz.org/reference/wrappers/Tooltip.html](https://panel-material-ui.holoviz.org/reference/wrappers/Tooltip.html)

- [https://mui.com/material-ui/react-tooltip/](https://mui.com/material-ui/react-tooltip/)

Example:

\>\>\> Tooltip(Button(label="Delete"), title="Remove this item")\

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
> [title="panel_material_ui.wrappers.base.Wrapper"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.wrappers.base.Wrapper](#panel.ui.wrappers.Wrapper):
> object
>
>

`arrow`` ``=`` ``Boolean(default=False,`` ``label='Arrow')`
Whether the tooltip has an arrow indicating the element it refers to.

`describe_child`` ``=`` ``Boolean(default=False,`` ``label='Describe`` ``child')`
Whether the tooltip acts as an accessible description rather than a
label. Use when the child already has a visible label and the tooltip
provides supplementary information.

`enter_delay`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=100,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Enter`` ``delay')`
The number of milliseconds to wait before showing the tooltip. This can
help avoid tooltips appearing on quick mouse passes.

`follow_cursor`` ``=`` ``Boolean(default=False,`` ``label='Follow`` ``cursor')`
Whether the tooltip follows the cursor position.

`leave_delay`` ``=`` ``Integer(bounds=(0,`` ``None),`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Leave`` ``delay')`
The number of milliseconds to wait before hiding the tooltip.

`open`` ``=`` ``Boolean(allow_None=True,`` ``label='Open')`
Explicitly control whether the tooltip is open. When None, the tooltip
is managed automatically on hover/focus. Set to True or False for
programmatic control.

`placement`` ``=`` ``Selector(default='right',`` ``label='Placement',`` ``names={},`` ``objects=['bottom-end',`` ``'bottom-start',`` ``'bottom',`` ``'left-end',`` ``'left-start',`` ``'left',`` ``'right-end',`` ``'right-start',`` ``'right',`` ``'top-end',`` ``'top-start',`` ``'top'])`
The placement of the tooltip relative to the child element.

`title`` ``=`` ``String(default='',`` ``label='Title')`
The text to display inside the tooltip.

class panel.ui.wrappers.Transition(object=None, **params)
Bases: [Wrapper](#panel.ui.wrappers.Wrapper)

The Transition wraps a child component with a transition effect that
plays when the child enters or exits. Supports multiple animation
variants including fade, grow, slide, zoom, and collapse.

References:

- [https://panel-material-ui.holoviz.org/reference/wrappers/Transition.html](https://panel-material-ui.holoviz.org/reference/wrappers/Transition.html)

- [https://mui.com/material-ui/transitions/](https://mui.com/material-ui/transitions/)

Example:

\>\>\> Transition(Button(label="Hello"), variant="fade", active=True)\

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
> [title="panel_material_ui.wrappers.base.Wrapper"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.wrappers.base.Wrapper](#panel.ui.wrappers.Wrapper):
> object
>
>

`active`` ``=`` ``Boolean(default=True,`` ``label='Active')`
Whether the child is shown (with transition). Set to False to animate
the child out, True to animate it in.

`duration`` ``=`` ``Integer(allow_None=True,`` ``bounds=(0,`` ``None),`` ``inclusive_bounds=(True,`` ``True),`` ``label='Duration')`
The duration of the transition in milliseconds. When None, the duration
is automatically calculated based on the element’s size.

`orientation`` ``=`` ``Selector(default='vertical',`` ``label='Orientation',`` ``names={},`` ``objects=['vertical',`` ``'horizontal'])`
The orientation of the collapse transition. Only applies when variant is
‘collapse’.

`placement`` ``=`` ``Selector(default='left',`` ``label='Placement',`` ``names={},`` ``objects=['down',`` ``'left',`` ``'right',`` ``'up'])`
The direction the child slides in from. Only applies when variant is
‘slide’.

`variant`` ``=`` ``Selector(default='fade',`` ``label='Variant',`` ``names={},`` ``objects=['collapse',`` ``'fade',`` ``'grow',`` ``'slide',`` ``'zoom'])`
The type of transition animation to apply.

class panel.ui.wrappers.Wrapper(object=None, **params)
Bases: [MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent)

Base class for wrapper components that decorate a single child element
with additional visual or behavioral embellishments.

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

`object`` ``=`` ``Child(allow_None=True,`` ``class_=<class`` ``'panel.viewable.Viewable'>,`` ``label='Object')`
The child component to wrap.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
