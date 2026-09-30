# Backdrop

```python
import panel as pn
import panel.ui

pn.extension()
```

The Backdrop signals a state change within the application and can be used for creating loaders, dialogs, and more. In its simplest form, the Backdrop component will add a dimmed layer over your application.

## Parameters:

### Core

* **`open`** (`boolean`): Whether the backdrop is visible.

---

The `Backdrop` can be opened and closed programmatically by setting the `open` parameter:

```python
open = pn.ui.Button(label='Open')
close = pn.ui.Button(label='Close')

dialog = pn.ui.Backdrop(close)

open.js_on_click(args={'dialog': dialog}, code="dialog.data.open = true")
close.js_on_click(args={'dialog': dialog}, code="dialog.data.open = false")

pn.ui.Column(open, dialog).preview()
```
