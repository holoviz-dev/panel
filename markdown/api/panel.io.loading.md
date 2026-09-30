# panel.io.loading module

This module contains functionality to make any Panel component look like
it is loading and disabled.

panel.io.loading.loading_css() → str
Returns the CSS that styles the loading indicator.

panel.io.loading.loading_css_classes() → list\[str\]
Returns the CSS classes that mark a component as loading.

panel.io.loading.loading_options() → dict\[str, Any\]
Returns the options that control the appearance of the loading
indicator, i.e. the spinner, color and max_height.

panel.io.loading.loading_resources(inline: bool = False, include_base: bool = True, dist_path: str \| None = None) → dict\[str, list\[str\]\]
Returns the resources required to render the loading indicator.

Parameters:
**inline: bool**
Whether to inline the stylesheets instead of linking them.

**include_base: bool**
Whether to include the base loading stylesheet.

**dist_path: str \| None**
The path the Panel distribution is served from.

Returns:
Dictionary containing stylesheet URLs and raw CSS.

panel.io.loading.start_loading_spinner(\*objects)
Changes the appearance of the specified panel objects to indicate that
they are loading.

This is done by

- adding a small spinner on top

- graying out the panel

- disabling the panel

- and changing the mouse cursor to a spinner when hovering over the
  panel

Parameters:
**objects: tuple**
The panels to add the loading indicator to.

panel.io.loading.stop_loading_spinner(\*objects)
Removes the loading indicating from the specified panel objects.

Parameters:
**objects: tuple**
The panels to remove the loading indicator from.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
