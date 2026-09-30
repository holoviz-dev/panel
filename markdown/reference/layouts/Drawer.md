# Drawer

```python
import panel as pn
import panel.ui

pn.extension()
```

The `Drawer` component (akin to a sidebar) provides ergonomic access to destinations in a site or app functionality.

## Parameters:
For details on other options for customizing the component see the layout and styling how-to guides.

### Core

* **`open`** (`boolean`): Whether the `Drawer` is open.

### Display

* **`anchor`** (`Literal["left", "right", "top", "bottom"]`): Where to position the `Drawer`.
* **`dock_position`** (`Literal["start", "middle", "end"]`): Position of the toggle tab along the drawer edge (only applies to the `docked` variant).
* **`inline`** (`boolean`): Whether the drawer is positioned inline within its parent container rather than fixed/absolute to the page. When `True`, the drawer participates in normal flow layout and pushes or shrinks sibling items.
* **`size`** (`int`): The width or height depending on whether the `Drawer` is rendered on the left/right or top/bottom respectively.
* **`variant`** (`Literal["temporary", "persistent", "permanent", "docked"]`): Whether the Drawer is temporary, persistent, permanent, or docked.

---

Temporary navigation drawers can toggle open or closed. Closed by default, the drawer opens temporarily above all other content until a section is selected.

The `Drawer` can be cancelled by clicking the overlay or pressing the Esc key. It closes when an item is selected, handled by controlling the `open` parameter.

```python
drawer = pn.ui.Drawer("I'm in a Drawer", size=300)

button = pn.ui.Button(label='Open Drawer')

button.js_on_click(args={'drawer': drawer}, code='drawer.data.open = true')

pn.ui.Container(button, drawer).preview()
```

`Drawer` also provides the `create_toggle` helper method to create a toggle that controls the `open` state of the drawer:

```python
drawer = pn.ui.Drawer("# My Drawer")

toggle = drawer.create_toggle(align='end')

pn.ui.Container(drawer, toggle, width_option='sm').preview()
```

### Anchor

Use the `anchor` parameter to specify which side of the screen the `Drawer` should originate from (the default value is `left`).

```python
container = pn.ui.Row()
for anchor in pn.ui.Drawer.param.anchor.objects:
    drawer = pn.ui.Drawer(f"I'm in a Drawer on the {anchor}", size=300, anchor=anchor)
    button = pn.ui.Button(label=anchor.upper(), width=100)
    button.js_on_click(args={'drawer': drawer}, code='drawer.data.open = true')
    container.extend([button, drawer])

container.preview()
```

### Persistent drawer

Persistent navigation drawers can toggle open or closed, but unlike a `temporary` they sit at the same elevation as the content and participate in the document flow.

This means that the `Drawer` should be placed in the correct position in the layout hierarchy:

```python
drawer = pn.ui.Drawer("## I'm in a Drawer", size=300, variant="persistent")

button = drawer.create_toggle(styles={'margin-left': 'auto'})
content = pn.ui.Row('# Title', button, sizing_mode='stretch_width')

pn.ui.Row(
    drawer, pn.ui.Container(content, width_option='sm'),
).preview()
```

### Docked drawer

A docked drawer renders a small toggle tab on the edge where it's anchored, allowing users to open and close it without needing a separate button. When closed, only the tab is visible; when open, the drawer slides out with the tab attached to close it again.

Use `dock_position` to control where the tab appears along the drawer edge (`"start"`, `"middle"`, or `"end"`):

```python
drawer = pn.ui.Drawer(
    "## Navigation",
    pn.ui.Button(label="Home"),
    pn.ui.Button(label="Settings"),
    size=250,
    variant="docked",
    anchor="left",
    dock_position="middle",
)

pn.ui.Row(drawer, pn.ui.Container("# Main Content", width_option='sm')).preview()
```

### Inline drawers

By default drawers are fixed or absolute to the page, overlaying other content. Setting `inline=True` makes the drawer participate in normal flow layout — when placed inside a `Row` or `Column` it pushes or shrinks sibling items rather than overlaying them.

`inline` is independent of `variant`, so all combinations are supported.

An inline docked drawer inside a `Row`:

```python
drawer = pn.ui.Drawer(
    "## Navigation",
    pn.ui.Button(label="Home"),
    pn.ui.Button(label="Settings"),
    size=250,
    variant="docked",
    anchor="left",
    inline=True,
)

pn.ui.Row(drawer, pn.ui.Container("# Main Content", width_option='sm'), sizing_mode='stretch_width').preview()
```

An inline persistent drawer:

```python
drawer = pn.ui.Drawer("## I'm in a Drawer", size=300, variant="persistent", inline=True)

button = drawer.create_toggle(styles={'margin-left': 'auto'}, color="light")
content = pn.ui.Row('# Title', sizing_mode='stretch_width')

pn.ui.Column(
    pn.ui.AppBar(drawer_toggle=button, title="Hello", sizing_mode="stretch_width"),
    pn.ui.Row(
        drawer, pn.ui.Container(content, width_option='sm'),
    )
).preview()
```
