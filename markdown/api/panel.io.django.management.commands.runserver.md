# panel.io.django.management.commands.runserver module

A `runserver` command which serves the project
with an ASGI server.

Django’s own development server is WSGI only, so it serves the Django
views of a project but not the Panel applications composed with them in
the ASGI application. This command replaces it with uvicorn running
`settings.ASGI_APPLICATION`, i.e.
`python`` ``manage.py`` ``runserver`
behaves as users expect. It is picked up by adding
`'panel.io.django'` to the
`INSTALLED_APPS`, before
`'django.contrib.staticfiles'`, which ships a
`runserver` command of its own.

class panel.io.django.management.commands.runserver.Command(stdout=None, stderr=None, no_color=False, force_color=False)
Bases: `Command`

Methods

|  |  |
|----|----|
| [add_arguments](#panel.io.django.management.commands.runserver.Command.add_arguments)(parser) | Entry point for subclassed commands to add custom arguments. |
| [run](#panel.io.django.management.commands.runserver.Command.run)(**options) | Run the server, using the autoreloader if needed. |

|             |     |
|-------------|-----|
| **on_bind** |     |

add_arguments(parser)
Entry point for subclassed commands to add custom arguments.

run(**options)
Run the server, using the autoreloader if needed.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
