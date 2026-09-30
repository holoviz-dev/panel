# TextEditor
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/widgets/TextEditor.ipynb)

------------------------------------------------------------------------

import panel as pn\
\
pn.extension('texteditor')\

The `TextEditor` widget provides a WYSIWYG
(what-you-see-is-what-you-get) rich text editor into a Panel application
which outputs HTML. The editor is built on top of the
[Quill.js](https://quilljs.com/)
library.

## Parameters:

For details on other options for customizing the component see the
[layout](../../../how_to/layout/index.md)
and [styling](../../../how_to/styling/index.md)
how-to guides.

- **`disabled`** (boolean): Whether the editor
  is disabled

- **`mode`** (str): Whether to display a
  `'toolbar'` or a
  `'bubble'` menu on highlight.

- **`on_keyup`** (boolean): Whether to update
  `value` on every key press or only upon loss
  of focus / hotkeys (`Ctrl+Enter` or
  `Cmd+Enter`). Defaults to
  `True`.

- **`placeholder`** (str): Placeholder output
  to render when the editor is empty.

- **`selection`** (dict): The current text
  selection in the editor, as
  `{"text":`` ``"..."}`
  when the user has a non-empty selection, else
  `{}`. Updates live.

- **`toolbar`** (boolean or list): Toolbar
  configuration either as a boolean toggle or a configuration specified
  as a list.

- **`value`** (str): The current HTML output of
  the widget if `on_keyup`. Otherwise, only
  updated on loss of focus or on `Ctrl+Enter` /
  `Cmd+Enter`.

- **`value_input`** (str): The current HTML
  output updated on every key press. Identical to
  `value` if
  `on_keyup`.

### Display

- **`label`** (str): The title of the widget

- **`name`** (str): Deprecated alias for
  `label`; use `label`
  instead.

------------------------------------------------------------------------

To construct a `TextEditor` editor widget we
must declare it explicitly and may provide a
`placeholder` as pure text or a
`value` as HTML:

wysiwyg = pn.widgets.TextEditor(placeholder='Enter some text')\
wysiwyg\

The current state of the editor output is reflected on the
`value` parameter:

wysiwyg.value\

The `value` may also be set:

wysiwyg.value = '\<h1\>A title\</h1\>'\

## Toolbar

The toolbar of the editor can be configured in a variety of ways, the
simplest of which is simply toggling it on and off by setting
`toolbar=True/False`. Beyond that we can
provide the formatting options to display in a number of configurations
which are explained in the
[quill.js documentation](https://quilljs.com/docs/modules/toolbar/#container). The examples
below

pn.config.sizing_mode = 'stretch_width'\
\
\# Flat list of options\
flat = pn.widgets.TextEditor(toolbar=\['bold', 'italic', 'underline'\])\
\
\# Grouped options\
grouped = pn.widgets.TextEditor(toolbar=\[\['bold', 'italic'\], \['link', 'image'\]\])\
\
\# Dropdown of options\
dropdown = pn.widgets.TextEditor(toolbar=\[{'size': \[ 'small', False, 'large', 'huge' \]}\])\
\
\# Full configuration\
full_config = pn.widgets.TextEditor(toolbar=\[\
  \['bold', 'italic', 'underline', 'strike'\],        \# toggled buttons\
  \['blockquote', 'code-block'\],\
\
  \[{ 'header': 1 }, { 'header': 2 }\],               \# custom button values\
  \[{ 'list': 'ordered'}, { 'list': 'bullet' }\],\
  \[{ 'script': 'sub'}, { 'script': 'super' }\],      \# superscript/subscript\
  \[{ 'indent': '-1'}, { 'indent': '+1' }\],          \# outdent/indent\
  \[{ 'direction': 'rtl' }\],                         \# text direction\
\
  \[{ 'size': \['small', False, 'large', 'huge'\] }\],  \# custom dropdown\
  \[{ 'header': \[1, 2, 3, 4, 5, 6, False\] }\],\
\
  \[{ 'color': \[\] }, { 'background': \[\] }\],          \# dropdown with defaults from theme\
  \[{ 'font': \[\] }\],\
  \[{ 'align': \[\] }\],\
\
  \['clean'\]                                         \# remove formatting button\
\])\
\
pn.Column(\
    pn.Row(flat, grouped, dropdown),\
    full_config\
)\

Instead of a toolbar we can also switch to
`'bubble'` mode which displays a hover menu
when highlighting the text:

pn.widgets.TextEditor(mode='bubble', value='Highlight me to edit formatting', margin=(40, 0, 0, 0), height=200, width=400)\

## Deferred commits with `on_keyup`

By default `value` updates on every keystroke.
Setting `on_keyup=False` defers updates to
`value` until the editor loses focus or the
user presses `Ctrl+Enter` /
`Cmd+Enter`. Use this when downstream callbacks
are expensive or when you want to batch edits. The
`value_input` parameter always streams live, so
you can bind to it for draft-state previews while committing only
finalized content through `value`.

deferred = pn.widgets.TextEditor(\
    placeholder='Type, then click away or press Ctrl/Cmd+Enter',\
    on_keyup=False,\
    height=150,\
)\
\
def show_value(v):\
    return f'**Committed \`value\`:**\n\n\`\`\`html\n{v}\n\`\`\`'\
\
def show_value_input(v):\
    return f'**Live \`value_input\`:**\n\n\`\`\`html\n{v}\n\`\`\`'\
\
pn.Column(\
    deferred,\
    pn.Row(\
        pn.bind(show_value, deferred.param.value),\
        pn.bind(show_value_input, deferred.param.value_input),\
    ),\
)\

## Tracking text selection

The `selection` parameter reflects the current
text selection in the editor. It updates live as the user highlights
text, and becomes an empty dict when the selection is cleared:

selectable = pn.widgets.TextEditor(\
    value='\<p\>Highlight any part of this sentence to see the selection update below.\</p\>',\
    height=150,\
)\
\
def show_selection(sel):\
    if not sel:\
        return '\*(nothing selected)\*'\
    return f'**Selected text:** \`{sel.get("text", "")}\`'\
\
pn.Column(\
    selectable,\
    pn.bind(show_selection, selectable.param.selection),\
)\

## Controls

The `TextEditor` widget exposes a number of
options which can be changed from both Python and Javascript. Try out
the effect of these parameters interactively:

editor = pn.widgets.TextEditor(placeholder='Enter some text')\
\
pn.Row(editor.controls(jslink=True, sizing_mode='fixed'), editor)\

------------------------------------------------------------------------
\| [Download this notebook from GitHub
(right-click to download).](https://raw.githubusercontent.com/holoviz/panel/main/examples/reference/widgets/TextEditor.ipynb)

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

[https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/widgets/TextEditor.ipynb](https://holoviz-dev.github.io/panelite-dev/lab?path=reference/classic/widgets/TextEditor.ipynb)

On this page
