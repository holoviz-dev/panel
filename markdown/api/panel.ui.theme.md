# panel.ui.theme module

The Material UI design and the themes it renders.

class panel.ui.theme.MaterialDesign(theme=None, **params)
Bases: [Material](panel.theme.material.md#panel.theme.material.Material)

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.theme.base.Design"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.theme.base.Design](panel.theme.base.md#panel.theme.base.Design):
> theme
>
>

class panel.ui.theme.MaterialUIDesign(theme=None, **params)
Bases:
[MaterialDesign](#panel.ui.theme.MaterialDesign)

Panel’s Material UI design defaults.

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.theme.base.Design"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.theme.base.Design](panel.theme.base.md#panel.theme.base.Design):
> theme
>
>

class panel.ui.theme.MuiDarkTheme(\*, base_css, bokeh_theme, css, name)
Bases: [MaterialDarkTheme](panel.theme.material.md#panel.theme.material.MaterialDarkTheme)

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.theme.base.DarkTheme"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.theme.base.DarkTheme](panel.theme.base.md#panel.theme.base.DarkTheme):
> base_css
>
> href="panel.theme.material.html#panel.theme.material.MaterialThemeMixin"
> class="reference internal"
> title="panel.theme.material.MaterialThemeMixin"> class="sourceCode python xref py py-class docutils literal notranslate">panel.theme.material.MaterialThemeMixin:
> css
>
>

`bokeh_theme`` ``=`` ``ClassSelector(class_=(<class`` ``'bokeh.themes.theme.Theme'>,`` ``<class`` ``'str'>),`` ``default=<bokeh.themes.theme.Theme`` ``object`` ``at`` ``0x1159f93d0>,`` ``label='Bokeh`` ``theme')`
A Bokeh Theme class that declares properties to apply to Bokeh models.
This is necessary to ensure that plots and other canvas based components
are styled appropriately.

class panel.ui.theme.MuiDefaultTheme(\*, base_css, bokeh_theme, css, name)
Bases: [MaterialDefaultTheme](panel.theme.material.md#panel.theme.material.MaterialDefaultTheme)

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.theme.base.DefaultTheme"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.theme.base.DefaultTheme](panel.theme.base.md#panel.theme.base.DefaultTheme):
> base_css
>
> href="panel.theme.material.html#panel.theme.material.MaterialThemeMixin"
> class="reference internal"
> title="panel.theme.material.MaterialThemeMixin"> class="sourceCode python xref py py-class docutils literal notranslate">panel.theme.material.MaterialThemeMixin:
> css
>
>

`bokeh_theme`` ``=`` ``ClassSelector(class_=(<class`` ``'bokeh.themes.theme.Theme'>,`` ``<class`` ``'str'>),`` ``default=<bokeh.themes.theme.Theme`` ``object`` ``at`` ``0x1159a7f80>,`` ``label='Bokeh`` ``theme')`
A Bokeh Theme class that declares properties to apply to Bokeh models.
This is necessary to ensure that plots and other canvas based components
are styled appropriately.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
