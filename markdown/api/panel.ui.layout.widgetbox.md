# panel.ui.layout.widgetbox module

A Material Paper with the disabled behavior of the classic WidgetBox.

class panel.ui.layout.widgetbox.WidgetBox(\*objects, **params)
Bases: [Paper](panel.ui.layout.md#panel.ui.layout.Paper)

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
> [class="reference internal"
> title="panel_material_ui.layout.base.Paper"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.Paper](panel.ui.layout.md#panel.ui.layout.Paper):
> margin, direction
>
>

`disabled`` ``=`` ``Boolean(default=False,`` ``label='Disabled')`
Whether the widgets in the box are disabled.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
