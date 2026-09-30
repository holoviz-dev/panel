# panel.ui.notifications module

The Material UI notification area.

class panel.ui.notifications.NotificationArea(\*, types, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, js_events, max_notifications, notifications, position, name)
Bases: [MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent),
[NotificationAreaBase](panel.io.notifications.md#panel.io.notifications.NotificationAreaBase)

Methods

|  |  |
|----|----|
| [demo](#panel.ui.notifications.NotificationArea.demo)(**params) | Generates a layout which allows demoing the component. |
| [send](#panel.ui.notifications.NotificationArea.send)(message\[, duration, type, background, icon\]) | Sends a notification to the frontend. |

|           |     |
|-----------|-----|
| **clear** |     |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> href="panel.io.notifications.html#panel.io.notifications.NotificationAreaBase"
> class="reference internal"
> title="panel.io.notifications.NotificationAreaBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.io.notifications.NotificationAreaBase:
> js_events, max_notifications, position
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

`notifications`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=(<class`` ``'panel_material_ui.notifications.MuiNotification'>,`` ``<class`` ``'dict'>),`` ``label='Notifications')`
List of notifications currently displayed in the notification area. Each
item is a MuiNotification or a dictionary representing a notification.

`types`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Types')`
Custom notification types. Each type is a dictionary with the following
keys: - ‘type’: The type of the notification. - ‘background’: The
background color of the notification. - ‘icon’: The icon of the
notification.

classmethod demo(**params)
Generates a layout which allows demoing the component.

send(message, duration=3000, type='default', background=None, icon=None)
Sends a notification to the frontend.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
