# panel.ui.widgets.debugger module

A Material Card holding a terminal that prints the logs of Panel
callbacks.

class panel.ui.widgets.debugger.Debugger(\*, \_number_of_errors, \_number_of_infos, \_number_of_warnings, formatter_args, level, logger_names, only_last, collapsed, collapsible, header, header_background, header_color, header_css_classes, hide_header, outlined, title, title_css_classes, title_variant, \_headers, \_names, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, objects, elevation, raised, square, variant, name)
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

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
