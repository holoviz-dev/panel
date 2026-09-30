# Skeleton

```python
import panel as pn
import panel.ui

pn.extension()
```

The `Skeleton` wraps a child component and displays an animated placeholder in its place while loading. When `active` is True the child is shown; when False the skeleton placeholder is rendered.

#### Parameters:

For details on other options for customizing the component see the [customization guides](https://panel-material-ui.holoviz.org/customization/index.html).

##### Core

* **`active`** (bool): Whether to show the child content. When False the skeleton placeholder is rendered; when True the child is displayed normally. Default is False.
* **`object`** (Viewable): The child component to wrap with the skeleton.

##### Display

* **`animation`** (str or None): The animation effect for the skeleton - options are 'pulse' (default), 'wave', or None (disabled).
* **`variant`** (str): Shape variant of the skeleton placeholder - options are 'text', 'circular', 'rectangular', or 'rounded' (default).

##### Styling

- **`sx`** (dict): Component level styling API for advanced customization
- **`theme_config`** (dict): Theming API for consistent design system integration

___

### Basic Usage

Wrap a component and toggle `active` to reveal it once loaded:

```python
toggle = pn.ui.Switch(value=False, label="Loaded")

skeleton = pn.ui.Skeleton(
    pn.ui.Button(label="Click me", variant="contained", color="primary"),
    active=toggle,
    variant="rounded",
)

pn.ui.Column(toggle, skeleton)
```

### Variants

The skeleton supports different shape variants to match the content it's replacing:

```python
toggle = pn.ui.Switch(value=False, label="Loaded")

pn.ui.Column(
    toggle,
    pn.ui.Column(
        pn.ui.Skeleton(
            pn.ui.Chip(label="Text", color="primary"),
            active=toggle,
            variant="text",
        ),
        pn.ui.Skeleton(
            pn.ui.Chip(label="Rounded", color="primary"),
            active=toggle,
            variant="rounded",
        ),
        pn.ui.Skeleton(
            pn.ui.Chip(label="Rectangular", color="primary"),
            active=toggle,
            variant="rectangular",
        ),
    ),
)
```

### Animation

Choose between pulse (default), wave, or no animation:

```python
toggle = pn.ui.Switch(value=False, label="Loaded")

pn.ui.Column(
    toggle,
    pn.ui.Skeleton(
        pn.ui.Button(label="Pulse", variant="contained"),
        active=toggle,
        animation="pulse",
        variant="rounded",
    ),
    pn.ui.Skeleton(
        pn.ui.Button(label="Wave", variant="contained"),
        active=toggle,
        animation="wave",
        variant="rounded",
    ),
    pn.ui.Skeleton(
        pn.ui.Button(label="None", variant="contained"),
        active=toggle,
        animation=None,
        variant="rounded",
    ),
)
```

### Revealing Content

Set `active=True` to reveal the wrapped child:

```python
toggle = pn.ui.Switch(value=False, label="Loaded")

pn.ui.Column(
    toggle,
    pn.ui.Row(
        pn.ui.Skeleton(
            pn.ui.Chip(label="Loading", color="warning"),
            active=toggle,
            variant="rounded",
        ),
    ),
)
```

### Responsive Sizing

When the wrapped component uses a responsive `sizing_mode` (e.g. `"stretch_width"`), set the same on the `Skeleton` so that **both** the placeholder and the revealed child fill the available space. A fixed-size child is hugged instead, so responsive and fixed cards can be mixed freely (for example inside a `Grid`).

```python
toggle = pn.ui.Switch(value=False, label="Loaded")

pn.ui.Column(
    toggle,
    pn.ui.Skeleton(
        pn.ui.Paper("Stretches to full width", height=80, sizing_mode="stretch_width"),
        active=toggle,
        sizing_mode="stretch_width",
    ),
    sizing_mode="stretch_width",
)
```

```python
```
