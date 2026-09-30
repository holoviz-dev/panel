# Terminal
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/widgets/Terminal.ipynb)

------------------------------------------------------------------------

import sys\
import uuid\
import logging\
import panel as pn\
\
pn.extension('terminal')\

The `Terminal` provides a way to display
outputs or logs from running processes as well as an interactive
terminal based on for example Bash, Python or IPython. The Terminal is
based on
[Xterm.js](https://xtermjs.org/)
which enables

- Terminal apps that just work: Xterm.js works with most terminal apps
  such as bash, vim and tmux, this includes support for curses-based
  apps and mouse event support

- Performance: Xterm.js is really fast, it even includes a
  GPU-accelerated renderer

- Rich unicode support: Supports CJK, emojis and IMEs

[https://xtermjs.org/](https://xtermjs.org/)

## Terminal Widget

### Parameters:

For details on other options for customizing the component see the
[layout](../../../how_to/layout/index.md)
and [styling](../../../how_to/styling/index.md)
how-to guides.

- **`clear`** (action): Clears the Terminal.

- **`options`** (dict) Initial Options for the
  Terminal Constructor. cf. [iterminaloptions](https://xtermjs.org/docs/api/terminal/interfaces/iterminaloptions/)

- **`output`** (str): System *output* written
  to the Terminal.

- **`value`** (str): User *input* received from
  the Terminal.

- **`write_to_console`** (boolean): If True
  output is additionally written to the server console. Default value is
  False.

### Methods

- **`write`**: Writes the specified string
  object to the Terminal.

## Terminal Subprocess

The `Terminal.subprocess` property makes it
easy for you to run subprocesses like `ls`,
`ls`` ``-l`,
`bash`, `python` and
`ipython` in the terminal.

### Parameters

- **`args`** (str, list): The arguments used to
  run the subprocess. This may be a string or a list. The string cannot
  contain spaces. See
  [subprocess.run](https://docs.python.org/3/library/subprocess.html) for more details.

- **`kwargs`** (dict): Any other arguments to
  run the subprocess. See
  [subprocess.run](https://docs.python.org/3/library/subprocess.html) for more details.

- **`running`** (boolean, readonly): Whether or
  not the subprocess is running. Defaults to False.

- **`run`** (action): Executes
  `subprocess.run` in a child process using the
  args and kwargs parameters provided as arguments or as parameter
  values on the instance. The child process is running in a *pseudo
  terminal* ([pty](https://docs.python.org/3/library/pty.html)) which is then connected to the
  Terminal.

- **`kill`** (action): Kills the subprocess if
  it is running.

#### Display

- **`label`** (str): The title of the widget

- **`name`** (str): Deprecated alias for
  `label`; use `label`
  instead.

------------------------------------------------------------------------

terminal = pn.widgets.Terminal(\
    "Welcome to the Panel Terminal!\nI'm based on xterm.js\n\n",\
    options={"cursorBlink": True},\
    height=300, sizing_mode='stretch_width'\
)\
\
terminal\

### Writing strings to the terminal

terminal.write("This is written directly to the terminal.\n")\
terminal.write("Danish Characters: æøåÆØÅ\n")\
terminal.write("Emoji: Python 🐍  Panel ❤️ 😊 \n")\
terminal.write("Links: https://panel.holoviz.org\n")\

184

### Writing stdout to the terminal

sys.stdout = terminal\
print("This print statement is redirected from stdout to the Panel Terminal")\
\
sys.stdout = sys.\_\_stdout\_\_\
print("This print statement is again redirected to the server console")\

### Logging to the terminal

logger = logging.getLogger("terminal")\
logger.setLevel(logging.DEBUG)\
\
stream_handler = logging.StreamHandler(terminal) \# NOTE THIS\
stream_handler.terminator = "  \n"\
formatter = logging.Formatter("%(asctime)s \[%(levelname)s\]: %(message)s")\
\
stream_handler.setFormatter(formatter)\
stream_handler.setLevel(logging.DEBUG)\
logger.addHandler(stream_handler)\

logger.info("Hello Info Logger")\

### Streaming to the terminal

We only do this to a reduced amount as you can reach a general rate
limit in the notebook.

for i in range(0, 50):\
    logger.info(uuid.uuid4()) \

### Run SubProcess and direct output to Terminal

terminal.subprocess.run("ls", "-l")\

Now let us review the output so far since a static rendering of this
page will not dynamically update the contents of the terminal displayed
above:

terminal\

### Clear the Terminal

terminal.clear()\

## Run an Interactive Process in the Terminal

You can run interactive processes like `bash`,
`python`, `ipython` or
similar.

subprocess_terminal = pn.widgets.Terminal(\
    options={"cursorBlink": True},\
    height=300, sizing_mode='stretch_width'\
)\
\
run_python = pn.widgets.Button(label="Run Python", color="success")\
run_python.on_click(\
    lambda x: subprocess_terminal.subprocess.run("python")\
)\
\
kill = pn.widgets.Button(label="Kill Python", color="danger")\
kill.on_click(\
    lambda x: subprocess_terminal.subprocess.kill()\
)\
\
pn.Column(\
    pn.Row(run_python, kill, subprocess_terminal.subprocess.param.running),\
    subprocess_terminal,\
    sizing_mode='stretch_both',\
    min_height=500\
)\

------------------------------------------------------------------------
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/widgets/Terminal.ipynb)

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

[https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/widgets/Terminal.ipynb](https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/widgets/Terminal.ipynb)

On this page
