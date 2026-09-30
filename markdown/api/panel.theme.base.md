# panel.theme.base module

class panel.theme.base.DarkTheme(\*, base_css, bokeh_theme, css, name)
Bases: [Theme](#panel.theme.base.Theme)

Baseclass for dark themes.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [title="panel.theme.base.Theme"> class="sourceCode python xref py py-class docutils literal notranslate">panel.theme.base.Theme](#panel.theme.base.Theme):
> css
>
>

`base_css`` ``=`` ``Filename(check_exists=True,`` ``default=PosixPath('/Users/runner/work/panel/panel/panel/theme/css/dark.css'),`` ``label='Base`` ``css',`` ``search_paths=[])`
A stylesheet declaring the base variables that define the color scheme.
By default this is inherited from a base class.

`bokeh_theme`` ``=`` ``ClassSelector(class_=(<class`` ``'bokeh.themes.theme.Theme'>,`` ``<class`` ``'str'>),`` ``default=<bokeh.themes.theme.Theme`` ``object`` ``at`` ``0x113892de0>,`` ``label='Bokeh`` ``theme')`
A Bokeh Theme class that declares properties to apply to Bokeh models.
This is necessary to ensure that plots and other canvas based components
are styled appropriately.

class panel.theme.base.DefaultTheme(\*, base_css, bokeh_theme, css, name)
Bases: [Theme](#panel.theme.base.Theme)

Baseclass for default or light themes.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [title="panel.theme.base.Theme"> class="sourceCode python xref py py-class docutils literal notranslate">panel.theme.base.Theme](#panel.theme.base.Theme):
> bokeh_theme, css
>
>

`base_css`` ``=`` ``Filename(check_exists=True,`` ``default=PosixPath('/Users/runner/work/panel/panel/panel/theme/css/default.css'),`` ``label='Base`` ``css',`` ``search_paths=[])`
A stylesheet declaring the base variables that define the color scheme.
By default this is inherited from a base class.

class panel.theme.base.Design(theme=None, **params)
Bases: `Parameterized`,
[ResourceComponent](panel.io.resources.md#panel.io.resources.ResourceComponent)

Methods

|  |  |
|----|----|
| [apply](#panel.theme.base.Design.apply)(viewable, root\[, isolated\]) | Applies the Design to a Viewable and all it children. |
| [apply_bokeh_theme_to_model](#panel.theme.base.Design.apply_bokeh_theme_to_model)(model\[, ...\]) | Applies the Bokeh theme associated with this Design system to a model. |
| [loading_css](#panel.theme.base.Design.loading_css)() | Returns the CSS that styles the loading indicator. |
| [loading_css_classes](#panel.theme.base.Design.loading_css_classes)() | Returns the CSS classes that mark a component as loading. |
| [loading_options](#panel.theme.base.Design.loading_options)() | Resolves the options that control the appearance of the loading indicator. |
| [loading_resources](#panel.theme.base.Design.loading_resources)(\[inline, include_base, ...\]) | Returns the resources required to render the loading indicator, e.g. when saving or converting an application. |
| [params](#panel.theme.base.Design.params)(viewable\[, doc\]) | Provides parameter values to apply the provided Viewable. |
| [resolve_component](#panel.theme.base.Design.resolve_component)(component) | Resolves the component to render in place of the provided component type. |
| [resolve_resources](#panel.theme.base.Design.resolve_resources)(\[cdn, extras, include_theme\]) | Resolves the resources required for this design component. |
| [resolve_widget](#panel.theme.base.Design.resolve_widget)(parameter) | Resolves the widget type to generate for a Parameter. |

**Parameter Definitions**

------------------------------------------------------------------------

`theme`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=<class`` ``'panel.theme.base.Theme'>,`` ``constant=True,`` ``label='Theme')`

apply(viewable: Viewable, root: Model, isolated: bool = True)
Applies the Design to a Viewable and all it children.

Parameters:
**viewable: Viewable**
The Viewable to apply the Design to.

**root: Model**
The root Bokeh model to apply the Design to.

**isolated: bool**
Whether the Design is applied to an individual component or embedded in
a template that ensures the resources, such as CSS variable definitions
and JS are already initialized.

apply_bokeh_theme_to_model(model: Model, theme_override=None)
Applies the Bokeh theme associated with this Design system to a model.

Parameters:
**model: bokeh.model.Model**
The Model to apply the theme on.

**theme_override: str \| None**
A different theme to apply.

classmethod loading_css() → str
Returns the CSS that styles the loading indicator.

classmethod loading_css_classes() → list\[str\]
Returns the CSS classes that mark a component as loading.

classmethod loading_options() → dict\[str, Any\]
Resolves the options that control the appearance of the loading
indicator.

The design system’s \_loading_options provide the defaults, any value
the user set explicitly takes precedence.

Returns:
Dictionary containing the spinner, color and max_height.

classmethod loading_resources(inline: bool = False, include_base: bool = True, dist_path: str \| None = None) → dict\[str, list\[str\]\]
Returns the resources required to render the loading indicator, e.g.
when saving or converting an application.

Parameters:
**inline: bool**
Whether to inline the stylesheets instead of linking them.

**include_base: bool**
Whether to include the base loading stylesheet. May be disabled if the
output already loads it, e.g. because it is rendered into a Panel
template.

**dist_path: str \| None**
The path the Panel distribution is served from. If not declared the CDN
is used and, when inlining, assets are embedded in the stylesheet.

Returns:
Dictionary containing stylesheet URLs and raw CSS.

params(viewable: Viewable, doc: Document \| None = None) → tuple\[dict\[str, t.Any\], dict\[str, t.Any\]\]
Provides parameter values to apply the provided Viewable.

Parameters:
**viewable: Viewable**
The Viewable to return modifiers for.

**doc: Document \| None**
Document the Viewable will be rendered into. Useful for caching any
stylesheets that are created.

Returns:
modifiers: Dict\[str, Any\]
Dictionary of parameter values to apply to the Viewable.

child_modifiers: Dict\[str, Any\]
Dictionary of parameter values to apply to the children of the Viewable.

classmethod resolve_component(component: T) → T
Resolves the component to render in place of the provided component
type.

Only exact matches in the component_mapping are substituted, since a
subclass may declare behavior the design system’s equivalent does not
implement.

Parameters:
**component: type**
The component type to find the equivalent for.

Returns:
The equivalent component in this design system, or the component

itself if the design system does not declare one.

resolve_resources(cdn: bool \| t.Literal\['auto'\] = 'auto', extras: dict\[str, dict\[str, str\]\] \| None = None, include_theme: bool = True) → ResourceTypes
Resolves the resources required for this design component.

Parameters:
**cdn: bool \| Literal\[‘auto’\]**
Whether to load resources from CDN or local server. If set to ‘auto’
value will be automatically determine based on global settings.

**extras: dict\[str, dict\[str, str\]\] \| None**
Additional resources to add to the bundle. Valid resource types include
js, js_modules and css.

**include_theme: bool**
Whether to include theme resources.

Returns:
Dictionary containing JS and CSS resources.

classmethod resolve_widget(parameter: Parameter) → type\[Any\] \| None
Resolves the widget type to generate for a Parameter.

Parameters:
**parameter: param.Parameter**
The Parameter to resolve a widget for.

Returns:
The widget type to render the Parameter with, or None if the

design system does not override the default resolution.

class panel.theme.base.Inherit
Bases: `object`

Singleton object to declare stylesheet inheritance.

class panel.theme.base.Theme(\*, base_css, bokeh_theme, css, name)
Bases: `Parameterized`

Theme objects declare the styles to switch between different color
modes. Each Design may declare any number of color themes.

modifiers
The modifiers override parameter values of Panel components.

**Parameter Definitions**

------------------------------------------------------------------------

`base_css`` ``=`` ``Filename(allow_None=True,`` ``check_exists=True,`` ``label='Base`` ``css',`` ``search_paths=[])`
A stylesheet declaring the base variables that define the color scheme.
By default this is inherited from a base class.

`bokeh_theme`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=(<class`` ``'bokeh.themes.theme.Theme'>,`` ``<class`` ``'str'>),`` ``label='Bokeh`` ``theme')`
A Bokeh Theme class that declares properties to apply to Bokeh models.
This is necessary to ensure that plots and other canvas based components
are styled appropriately.

`css`` ``=`` ``Filename(allow_None=True,`` ``check_exists=True,`` ``label='Css',`` ``search_paths=[])`
A stylesheet that overrides variables specifically for the Theme
subclass. In most cases, this is not necessary.

panel.theme.base.design_template_variables() → dict\[str, Any\]
Returns the page template variables declared by the currently active
design system.

panel.theme.base.resolve_component(component: T) → T
Resolves the component to render in place of the provided component type
given the currently active design system.

Parameters:
**component: type**
The component type to find the equivalent for.

Returns:
The equivalent component in the active design system, or the

component itself if there is none.

panel.theme.base.resolve_design(design: str \| type\[Design\]) → type\[Design\]
Resolves the Design class given its name.

Parameters:
**design: str \| type\[Design\]**
The name of the Design or the Design itself.

Returns:
The resolved Design class.

panel.theme.base.resolve_widget(parameter: param.Parameter) → type\[Viewable\] \| None
Resolves the widget type to generate for a Parameter given the currently
active design system.

Parameters:
**parameter: param.Parameter**
The Parameter to resolve a widget for.

Returns:
The widget type declared by the active design system, or None if it

does not override the default resolution.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
