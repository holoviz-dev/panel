# panel.command.migrate module

CLI subcommand rewriting classic Panel source code to the
`panel.ui` namespace (plan §10.1).

The heavy lifting lives in
`panel.command._migrate`, which is only
imported inside [Migrate.invoke()](#panel.command.migrate.Migrate.invoke):
`libcst` is an optional dependency
(`pip`` ``install`` ``panel[migrate]`),
and importing it eagerly here would make it a hard dependency of every
`panel` command, including ones that have
nothing to do with migration.

class panel.command.migrate.Migrate(parser: ArgumentParser)
Bases: `Subcommand`

Subcommand rewriting classic Panel source code to the panel.ui
namespace.

Methods

|  |  |
|----|----|
| [invoke](#panel.command.migrate.Migrate.invoke)(args) | Takes over main program flow to perform the subcommand. |

invoke(args: argparse.Namespace) → int
Takes over main program flow to perform the subcommand.

*This method must be implemented by subclasses.* subclassed overwritten
methods return different types: bool: Build None: FileOutput (subclassed
by HTML, SVG and JSON. PNG overwrites FileOutput.invoke method), Info,
Init, Sampledata, Secret, Serve, Static

Args:
args (argparse.Namespace) : command line arguments for the subcommand to
parse

Raises:
NotImplementedError

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
