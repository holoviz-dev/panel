# panel.io.resource_spec module

Derives the client-side resource specification for component classes.

The specification is the payload the browser needs in order to load a
component’s external libraries on demand. It is derived entirely from
the declarations components already make
(`__javascript_raw__`,
`__javascript_modules_raw__`,
`__javascript_module_exports__`,
`__css_raw__` and
`__js_skip__`), so third-party component
authors get lazy loading without any new API.

The same specification feeds both delivery paths:

- the lazy path, where it is carried by the
  `external_resources` property of a model
  instance and resolved by the client-side registry, and

- the eager path, where `pn.extension` renders
  the script and link tags into the page and the templates call
  `declare()` on the registry with the specs it
  just satisfied.

Generating both from one function is what keeps them from drifting.

panel.io.resource_spec.declared_specs(mode: MODES \| None = None) → dict\[str, t.Any\]
The resources the eager path has already satisfied.

Rendered into the page (and the notebook bootstrap) as a
`declare()` call so that the registry knows
about them without having to infer it from the DOM, which is the only
thing that works in `inline` mode, where the
libraries were inlined and have no urls at all.

panel.io.resource_spec.lazy_load_available(notebook: bool = False) → bool
Whether a component that was not declared can still get its resources.

False when lazy loading was switched off, and for self-contained
`inline` output, where there is nothing left to
inline after the fact and the component would silently fall back to the
CDN. Notebooks are exempt from the latter: their output is never
self-contained anyway.

panel.io.resource_spec.resource_spec(cls: type, mode: MODES \| None = None) → dict\[str, t.Any\] \| None
Builds the client-side resource specification for a component class.

Groups the class’ `__javascript__` urls by the
global they provide (from `__js_skip__`),
resolves them for the active resource mode via the same
`bundled_files`/`adjust_paths`
machinery the eager path uses, and appends
`__javascript_modules__` (with their
`__javascript_module_exports__` names) and
`__css__`.

Parameters:
**cls: type**
A Bokeh model class, or a
`ReactiveHTML`/`ReactiveESM`
subclass, whose resources are declared on the Panel class.

**mode: MODES \| None**
Resource mode to resolve urls for, defaulting to the active one.

Returns:
The specification, or None if the class declares no resources or lazy

loading is disabled.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
