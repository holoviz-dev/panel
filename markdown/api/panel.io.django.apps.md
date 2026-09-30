# panel.io.django.apps module

The Django application configuration of the Panel integration.

Adding `'panel.io.django'` to the
`INSTALLED_APPS` is only needed to pick up the
`runserver` management command that serves the
ASGI application, see
`panel.io.django.management.commands.runserver`.

class panel.io.django.apps.PanelConfig(app_name, app_module)
Bases: `AppConfig`

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
