# panel.io.django package

## Subpackages

- [panel.io.django.management package](panel.io.django.management.md)
  - [Subpackages](panel.io.django.management.md#subpackages)
    - [panel.io.django.management.commands
      package](panel.io.django.management.commands.md)
      - [Submodules](panel.io.django.management.commands.md#submodules)
      - [Module contents](panel.io.django.management.commands.md#module-panel.io.django.management.commands)
  - [Module contents](panel.io.django.management.md#module-panel.io.django.management)

## Submodules

- [panel.io.django.apps module](panel.io.django.apps.md)
  - [PanelConfig](panel.io.django.apps.md#panel.io.django.apps.PanelConfig)

## Module contents

Native Django integration for Panel applications.

Panel applications are served by
[panel.io.asgi.PanelASGI](panel.io.asgi.md#panel.io.asgi.PanelASGI),
which is composed with Django’s own ASGI application. The routes Panel
owns, i.e. the application documents,
`/autoload.js`, the websocket, BokehJS and
component resources, are dispatched to Panel and everything else is
handed to Django.

This replaces the `bokeh-django`/Channels based
integration, which is no longer needed. The
`document`,
`autoload`,
`directory`,
`static_extensions`,
`with_request` and
`with_url_args` helpers are kept so that an
existing project only has to replace its Channels routing with
[panel.io.django.get_asgi_application()](#panel.io.django.get_asgi_application).

This module is also a Django application. Adding it to the
`INSTALLED_APPS`, before
`'django.contrib.staticfiles'`, replaces the
WSGI only `runserver` command with one that
serves the ASGI application with uvicorn.

class panel.io.django.PanelDjangoASGI(applications: Mapping\[str, BkApplication\], \*, django_app: t.Any = None, document_paths: Iterable\[str\] \| None = None, **kwargs)
Bases: [PanelASGI](panel.io.asgi.md#panel.io.asgi.PanelASGI)

An ASGI3 application serving Panel application(s) alongside a Django
application.

Requests for the routes Panel owns, i.e. the applications and their
websocket, autoload and resource endpoints, are served by Panel; every
other request is handed to the Django application.

Parameters:
**applications: Mapping\[str, Application\]**
The application(s) to serve.

**django_app: ASGI application**
The application to hand all other requests to. Defaults to
`django.core.asgi.get_asgi_application()`.

**document_paths: Iterable\[str\] \| None**
The application paths that serve their rendered document. Paths that are
not listed are only served for embedding, i.e. Django renders the page
on the application path itself. Defaults to all applications.

**kwargs: dict**
Additional keyword arguments to pass to
`PanelASGI`.

Attributes:
**django_app**

Methods

|  |  |
|----|----|
| `__call__`(scope, receive, send) | Call self as a function. |
| [handles](#panel.io.django.PanelDjangoASGI.handles)(scope) | Whether this application owns the given ASGI scope. |

handles(scope: Scope) → bool
Whether this application owns the given ASGI scope. Allows composing
`PanelASGI` with another ASGI application, e.g.
Django or FastAPI.

class panel.io.django.PanelExtensionFinder(app_names=None, \*args, **kwargs)
Bases: `BaseFinder`

A staticfiles finder which serves the resources of Panel and Bokeh
extensions.

Only needed if the Django development server is used to serve the static
files, e.g. because the applications are embedded in Django views with
`autoload`. Add it to the
`STATICFILES_FINDERS` in the Django settings:

>
>
> STATICFILES_FINDERS = \[
> ‘django.contrib.staticfiles.finders.FileSystemFinder’,
> ‘django.contrib.staticfiles.finders.AppDirectoriesFinder’,
> ‘panel.io.django.PanelExtensionFinder’,
>
> \]
>
>

Methods

|  |  |
|----|----|
| [find](#panel.io.django.PanelExtensionFinder.find)(path\[, find_all\]) | Given a relative file path, find an absolute file path. |
| [find_location](#panel.io.django.PanelExtensionFinder.find_location)(path\[, prefix, as_components\]) | Find the absolute path of a resource given a relative path. |
| [list](#panel.io.django.PanelExtensionFinder.list)(ignore_patterns) | Lists all the extension resources, so that they are collected by the `collectstatic` management command. |

|           |     |
|-----------|-----|
| **check** |     |

find(path, find_all=False, **kwargs)
Given a relative file path, find an absolute file path.

If the `find_all` parameter is False (default)
return only the first found file path; if True, return a list of all
found file paths.

classmethod find_location(path, prefix=None, as_components=False)
Find the absolute path of a resource given a relative path.

Args:
path (str): relative path to the resource prefix (str): if given,
verifies that path starts with prefix

>
>
> else returns None
>
>

as_components (bool): If True return a tuple of
(artifacts_dir, artifact_path) rather than the absolute path. Used when
the components have to be passed to Django’s static.serve view
separately.

list(ignore_patterns)
Lists all the extension resources, so that they are collected by the
`collectstatic` management command.

class panel.io.django.Routing(url: str, app: ApplicationLike, \*, document: bool = False, autoload: bool = False)
Bases: `object`

Declares a Panel application served on a URL.

Parameters:
**url: str**
The URL to serve the application on.

**app: Application, callable or path**
The application to serve, either a Bokeh/Panel
`Application`, a function that modifies a
Document or the path to an application script, notebook or directory.

**document: bool**
Whether to serve the rendered application on the URL itself.

**autoload: bool**
Whether to serve the application for embedding in a Django view, i.e. on
`<url>/autoload.js`.

panel.io.django.autoload(url: str, app: ApplicationLike) → Routing
Declares an application to embed in a Django view, i.e. it is served on
`<url>/autoload.js` and rendered by the script
the `bokeh.embed.server_document` helper
generates.

panel.io.django.directory(\*apps_paths: str \| PathLike) → list\[Routing\]
Declares all applications in one or more directories, serving each of
them as a full page on the URL matching its filename.

panel.io.django.document(url: str, app: ApplicationLike) → Routing
Declares an application to serve as a full page on the given URL.

panel.io.django.get_asgi_application(routings: Routing \| Sequence\[Routing \| Sequence\[Routing\]\], \*, django_app: t.Any = None, **kwargs) → PanelDjangoASGI
Builds the ASGI application serving the declared Panel application(s)
alongside a Django application.

Declare it as the ASGI application of the project, e.g. in
`project/asgi.py`:

>
>
> import os
>
> from panel.io.django import document, get_asgi_application
>
> os.environ.setdefault(‘DJANGO_SETTINGS_MODULE’, ‘project.settings’)
>
> import my_app.pn_app as pn_app
>
> application = get_asgi_application(\[document(‘sliders’,
> pn_app.app)\])
>
>

and serve it with an ASGI server, e.g.
`uvicorn`` ``project.asgi:application`.
Adding `'panel.io.django'` to the
`INSTALLED_APPS` makes
`manage.py`` ``runserver`
do that as well, since Django’s own development server is WSGI only.

Parameters:
**routings: Routing \| list\[Routing\]**
The application(s) to serve, declared with
`document`, `autoload`
or `directory`.

**django_app: ASGI application**
The application to hand all non-Panel requests to. Defaults to
`django.core.asgi.get_asgi_application()`.

**kwargs: dict**
Additional keyword arguments to pass to the
`PanelASGI` application, including the
authentication arguments applied by
`panel.io.auth.configure_auth`, e.g.
`basic_auth` or
`oauth_provider`.

Returns:
The ASGI application.

panel.io.django.static_extensions(prefix: str = '/static/extensions/')
Returns the urlpatterns serving the resources of Panel and Bokeh
extensions from Django.

Only needed if the applications are embedded in Django views with
`autoload` and Django serves the static files.

panel.io.django.with_request(handler)
Wraps an application function so that it is called with the HTTP request
that created the session in addition to the Document.

panel.io.django.with_url_args(handler)
Wraps an application function so that it is called with the parameters
captured by the route it is served on, e.g. an application declared on
`/user/{name}` is called with the
`name` keyword argument.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
