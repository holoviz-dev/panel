# panel.models.resource module

Declares the property that carries a component’s resource specification.

The resource bearing models do not share a single base:
`HTMLBox` covers most of them, but
`KaTeX` derives from Bokeh’s
`Markup`,
`FileDropper` from
`InputWidget`, `Modal`
from `Column` and the plot models from
`LayoutDOM`. The property is therefore declared
through a mixin, the same pattern Bokeh uses for
`FillProps` and friends.

class panel.models.resource.ExternalResourcesMixin(\*args: Any, **kwargs: Any)
Bases: `HasProps`

Mixin declaring the `external_resources`
property.

Bokeh only serializes properties that were explicitly set, so the
specification is derived and assigned at construction time. It can be
passed explicitly instead, which is what the
`ReactiveHTML` and
`ReactiveESM` models do: their resources are
declared on the *Panel* class while the Bokeh model class is shared.

Attributes:
**external_resources**
Client-side specification of the external libraries and stylesheets this
component needs, resolved by the resource registry in panel.js when the
component is rendered.

external_resources
Client-side specification of the external libraries and stylesheets this
component needs, resolved by the resource registry in panel.js when the
component is rendered.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
