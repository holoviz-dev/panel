# panel.io.auth module

Transport neutral authentication support.

Panel implements authentication as Tornado
`RequestHandler` classes, covering fifteen
OAuth providers, PKCE, token refresh, basic auth and PAM. Rather than
reimplementing those flows for ASGI transports this module runs the very
same handlers headlessly, against a Tornado request synthesized from a
framework neutral `ServerRequest`, and
translates the response they write into an ASGI response.

Tornado therefore remains the only implementation minting and validating
Panel’s signed cookies, which is what makes a session established
against the Tornado server usable by an ASGI server and vice versa.

class panel.io.auth.PanelAuthPolicy(provider: AuthProvider, server_config: dict\[str, t.Any\] \| None = None, prefix: str = '')
Bases: `AuthPolicy`

An `AuthPolicy` which authenticates requests
with a Panel `AuthProvider` and serves its
login and logout endpoints.

Parameters:
**provider: AuthProvider**
The provider whose handlers implement the authentication flow.

**server_config: dict**
Per-server configuration, e.g. the `basic_auth`
credentials, which the handlers look up on
`state._server_config`.

**prefix: str**
The URL prefix the server, and therefore the login and logout endpoints,
are served under.

Attributes:
[routes](#panel.io.auth.PanelAuthPolicy.routes)
The routes the provider’s login and logout endpoints are served on, as
`(pattern,`` ``handler)`
pairs.

Methods

|  |  |
|----|----|
| [authenticate](#panel.io.auth.PanelAuthPolicy.authenticate)(request) | Return the authenticated user for a request, or `None`. |
| [run](#panel.io.auth.PanelAuthPolicy.run)(handler_cls, request\[, body\]) | Executes a Tornado request handler headlessly and returns the response it wrote. |

async authenticate(request: ServerRequest) → t.Any \| None
Return the authenticated user for a request, or
`None`.

property routes: list\[tuple\[str, RouteHandler\]\]
The routes the provider’s login and logout endpoints are served on, as
`(pattern,`` ``handler)`
pairs.

async run(handler_cls: type\[RequestHandler\], request: ServerRequest, body: bytes = b'') → AuthResponse
Executes a Tornado request handler headlessly and returns the response
it wrote.

Parameters:
**handler_cls: type\[RequestHandler\]**
The handler class to execute.

**request: ServerRequest**
The request to serve.

**body: bytes**
The request body, e.g. a submitted login form.

panel.io.auth.configure_auth(basic_auth: str \| None = None, oauth_provider: str \| None = None, oauth_key: str \| None = None, oauth_secret: str \| None = None, oauth_redirect_uri: str \| None = None, oauth_extra_params: Mapping\[str, str\] = {}, oauth_error_template: str \| None = None, cookie_path: str = '/', cookie_secret: str \| None = None, oauth_encryption_key: str \| bytes \| None = None, oauth_jwt_user: str \| None = None, oauth_refresh_tokens: bool \| None = None, oauth_guest_endpoints: list\[str\] \| None = None, oauth_optional: bool \| None = None, login_endpoint: str \| None = None, logout_endpoint: str \| None = None, login_template: str \| None = None, logout_template: str \| None = None, basic_login_template: str \| None = None) → tuple\[AuthProvider \| None, dict\[str, t.Any\]\]
Applies authentication configuration and builds the
`AuthProvider` serving it, if any. Shared by
all transports.

Returns:
The AuthProvider, if authentication was requested, and the per-server

configuration the provider’s handlers need.

panel.io.auth.pop_auth_kwargs(kwargs: dict\[str, Any\]) → dict\[str, Any\]
Extracts the authentication related arguments from a set of server
keyword arguments, so they can be applied with
`configure_auth`.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
