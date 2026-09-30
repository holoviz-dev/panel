# panel.io.fastapi module

Native FastAPI integration for Panel applications.

Panel applications are served by
[panel.io.asgi.PanelASGI](panel.io.asgi.md#panel.io.asgi.PanelASGI),
a framework neutral ASGI application. Rather than registering one route
per application on the FastAPI app, the ASGI application is installed as
a middleware which claims the paths Panel owns and delegates everything
else to FastAPI. This makes the integration insensitive to the order in
which Panel and FastAPI routes are declared.

panel.io.fastapi.add_application(path: str, app: FastAPI, title: str = 'Panel App', location: bool \| Location = True, admin: bool = False, **kwargs)
Decorator that adds a Panel app to a FastAPI application.

Parameters:
**path: str**
The path to serve the application on.

**app: FastAPI**
FastAPI app to add Panel application(s) to.

title : str
An HTML title for the application.

location : boolean or panel.io.location.Location
Whether to create a Location component to observe and set the URL
location.

**admin: boolean (default=False)**
Whether to enable the admin panel

****kwargs:**
Additional keyword arguments to pass to the PanelASGI application

panel.io.fastapi.add_applications(panel: TViewableFuncOrPath \| dict\[str, TViewableFuncOrPath\], app: FastAPI \| None = None, title: str \| dict\[str, str\] \| None = None, location: bool \| Location = True, admin: bool = False, session_history: int \| None = None, liveness: bool \| str = False, **kwargs) → PanelFastAPI
Adds application(s) to an existing FastAPI application.

Parameters:
**app: FastAPI**
FastAPI app to add Panel application(s) to.

**panel: Viewable, function or {str: Viewable}**
A Panel object, a function returning a Panel object or a dictionary
mapping from the URL slug to either.

title : str or {str: str} (optional, default=None)
An HTML title for the application or a dictionary mapping from the URL
slug to a customized title.

location : boolean or panel.io.location.Location
Whether to create a Location component to observe and set the URL
location.

**admin: boolean (default=False)**
Whether to enable the admin panel

**session_history: int (optional, default=None)**
The amount of session history to accumulate. If set to non-zero and
non-None value will launch an endpoint at /session_info, which returns
information about the session history.

**liveness: bool \| str (optional, default=False)**
Whether to add a liveness endpoint. If a string is provided then this
will be used as the endpoint, otherwise the endpoint will be hosted at
/liveness.

****kwargs:**
Additional keyword arguments to pass to the PanelASGI application

panel.io.fastapi.dispatch_fastapi(conn, events: list\[DocumentPatchedEvent\] \| None = None, msg: Message \| None = None)
Dispatches a message or set of events to an ASGI websocket transport.

panel.io.fastapi.get_server(panel: TViewableFuncOrPath \| dict\[str, TViewableFuncOrPath\], port: int \| None = 0, show: bool = True, start: bool = False, title: str \| dict\[str, str\] \| None = None, location: bool \| Location = True, admin: bool = False, **kwargs) → Server
Creates a FastAPI server running the provided Panel application(s).

Parameters:
**panel: Viewable, function or {str: Viewable}**
A Panel object, a function returning a Panel object or a dictionary
mapping from the URL slug to either.

**port: int (optional, default=0)**
Allows specifying a specific port.

show : boolean (optional, default=True)
Whether to open the server in a new browser tab on start

start : boolean(optional, default=False)
Whether to start the Server.

title : str or {str: str} (optional, default=None)
An HTML title for the application or a dictionary mapping from the URL
slug to a customized title.

location : boolean or panel.io.location.Location
Whether to create a Location component to observe and set the URL
location.

**admin: boolean (default=False)**
Whether to enable the admin panel

**liveness: bool \| str (optional, default=False)**
Whether to add a liveness endpoint. If a string is provided then this
will be used as the endpoint, otherwise the endpoint will be hosted at
/liveness.

**session_history: int (optional, default=None)**
The amount of session history to accumulate. If set to non-zero and
non-None value will launch an endpoint at /session_info, which returns
information about the session history.

****kwargs:**
Additional keyword arguments to pass to the PanelASGI application

panel.io.fastapi.serve(panels: TViewableFuncOrPath \| dict\[str, TViewableFuncOrPath\], port: int = 0, address: str \| None = None, websocket_origin: str \| list\[str\] \| None = None, loop: asyncio.AbstractEventLoop \| None = None, show: bool = True, start: bool = True, title: str \| None = None, location: bool = True, threaded: bool = False, admin: bool = False, session_history: int \| None = None, liveness: bool \| str = False, **kwargs) → StoppableThread \| Server
Allows serving one or more panel objects on a single server. The panels
argument should be either a Panel object or a function returning a Panel
object or a dictionary of these two. If a dictionary is supplied the
keys represent the slugs at which each app is served, e.g. serve({‘app’:
panel1, ‘app2’: panel2}) will serve apps at /app and /app2 on the
server.

Reference: [https://panel.holoviz.org/user_guide/Server_Configuration.html#serving-multiple-apps](https://panel.holoviz.org/user_guide/Server_Configuration.html#serving-multiple-apps)

Parameters:
**panel: Viewable, function or {str: Viewable or function}**
A Panel object, a function returning a Panel object or a dictionary
mapping from the URL slug to either.

**port: int (optional, default=0)**
Allows specifying a specific port

address : str
The address the server should listen on for HTTP requests.

**websocket_origin: str or list(str) (optional)**
A list of hosts that can connect to the websocket.

This is typically required when embedding a server app in an external
web site.

If None, “localhost” is used.

loop : asyncio.AbstractEventLoop (optional)
The event loop to run the Server on

show : boolean (optional, default=True)
Whether to open the server in a new browser tab on start

start : boolean(optional, default=True)
Whether to start the Server

**title: str or {str: str} (optional, default=None)**
An HTML title for the application or a dictionary mapping from the URL
slug to a customized title

location : boolean or panel.io.location.Location
Whether to create a Location component to observe and set the URL
location.

**threaded: boolean (default=False)**
Whether to start the server on a new Thread

**admin: boolean (default=False)**
Whether to enable the admin panel

**liveness: bool \| str (optional, default=False)**
Whether to add a liveness endpoint. If a string is provided then this
will be used as the endpoint, otherwise the endpoint will be hosted at
/liveness.

**session_history: int (optional, default=None)**
The amount of session history to accumulate. If set to non-zero and
non-None value will launch an endpoint at /session_info, which returns
information about the session history.

**kwargs: dict**
Additional keyword arguments to pass to the PanelASGI application

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
