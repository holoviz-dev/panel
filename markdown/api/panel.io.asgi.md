# panel.io.asgi module

A framework neutral ASGI implementation for serving Panel applications.

`PanelASGI` extends Bokeh’s
`BokehASGI` with the routing, session and
rendering behavior Panel’s Tornado server provides, i.e. wildcard
routes, a custom index page, `--static-dirs`
mounts, component resources, liveness endpoints and session reuse. It is
the shared core behind
[panel.io.fastapi](panel.io.fastapi.md#module-panel.io.fastapi),
[panel.io.django](panel.io.django.md#module-panel.io.django)
and
`panel`` ``serve`` ``--server`` ``asgi`.

class panel.io.asgi.PanelASGI(applications: t.Any, \*, prefix: str = '', index: str \| None = '/Users/runner/work/panel/panel/panel/io/../\_templates/index.html', index_enabled: bool = True, ico_path: str \| os.PathLike \| None = None, static_dirs: Mapping\[str, str\] \| None = None, liveness: bool \| str = False, mem_log_frequency_milliseconds: int = 0, session_history: int \| None = None, extra_routes: Sequence\[tuple\[str, RouteHandler\]\] \| None = None, auth_provider: AuthProvider \| None = None, auth_policy: AuthPolicy \| None = None, server_config: dict\[str, t.Any\] \| None = None, **kwargs)
Bases: `BokehASGI`

An ASGI3 application serving one or more Panel applications.

Parameters:
**applications: Mapping\[str, Application\] \| Application \| callable \| path**
The application(s) to serve, either already built Bokeh/Panel
Application objects or anything
`BokehServerCore` accepts.

**prefix: str**
URL prefix all routes are served under.

**index: str \| None**
Path to a template rendered on the root URL when it is not itself an
application. Defaults to Panel’s own index page.

**index_enabled: bool**
Whether to render an index page on the root URL at all.

**ico_path: str \| os.PathLike \| None**
Path to the favicon served on `/favicon.ico`.
The string `'none'` disables the endpoint.

**static_dirs: Mapping\[str, str\] \| None**
Mapping from URL slug to a local directory to serve.

**liveness: bool \| str**
Whether to serve a liveness endpoint and, if a string is given, the
endpoint to serve it on.

**mem_log_frequency_milliseconds: int**
How often to log memory usage, 0 to disable. Requires psutil.

**session_history: int \| None**
If set, enables session history tracking and serves it on
`/session_info`.

**extra_routes: Sequence\[tuple\[str, RouteHandler\]\] \| None**
Additional routes as
`(pattern,`` ``handler)`
pairs. Patterns are regular expressions matched against the
prefix-relative path.

**auth_provider: AuthProvider \| None**
Provider implementing authentication, i.e. the login and logout
endpoints and the user lookup. Ignored if an
`auth_policy` is given.

**auth_policy: AuthPolicy \| None**
Policy used to authenticate HTTP and websocket requests.

**server_config: dict\[str, Any\] \| None**
Per-server configuration, e.g. the `basic_auth`
credentials, looked up by the authentication handlers.

Methods

|  |  |
|----|----|
| `__call__`(scope, receive, send) | Call self as a function. |
| [handles](#panel.io.asgi.PanelASGI.handles)(scope) | Whether this application owns the given ASGI scope. |

handles(scope: Scope) → bool
Whether this application owns the given ASGI scope. Allows composing
`PanelASGI` with another ASGI application, e.g.
Django or FastAPI.

panel.io.asgi.build_asgi_app(panel: TViewableFuncOrPath \| dict\[str, TViewableFuncOrPath\], title: str \| dict\[str, str\] \| None = None, location: bool \| Location = True, admin: bool = False, warm: bool = False, websocket_origin: str \| list\[str\] \| None = None, **kwargs) → PanelASGI
Builds a `PanelASGI` application from one or
more Panel objects.

Parameters:
**panel: Viewable, function or {str: Viewable}**
A Panel object, a function returning a Panel object or a dictionary
mapping from the URL slug to either.

**title: str or {str: str}**
An HTML title for the application or a dictionary mapping from the URL
slug to a customized title.

**location: boolean or panel.io.location.Location**
Whether to create a Location component to observe and set the URL
location.

**admin: boolean**
Whether to enable the admin panel.

**warm: boolean**
Whether to run the applications before serving them to ensure all
imports and caches are fully warmed up.

**websocket_origin: str or list(str)**
A list of hosts that can connect to the websocket.

**kwargs: dict**
Additional keyword arguments to pass to
`PanelASGI`, including the authentication
arguments applied by
`panel.io.auth.configure_auth`, e.g.
`basic_auth` or
`oauth_provider`.

panel.io.asgi.dispatch_asgi(conn, events: list\[DocumentPatchedEvent\] \| None = None, msg: Message \| None = None)
Dispatches a message or set of events to an ASGI websocket transport.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
