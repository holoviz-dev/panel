# CheckBoxGroup

:class: tip

`pn.ui.CheckBoxGroup` supersedes `pn.widgets.CheckBoxGroup`, which remains available and is documented in the [classic CheckBoxGroup reference](../classic/widgets/CheckBoxGroup.md).
:::

```python
import panel as pn
import panel.ui

pn.extension()
```

The `CheckBoxGroup` widget allows users to select multiple options from a list by checking the corresponding checkboxes. This widget is part of the multi-option selection family, which includes `MultiSelect`, `CrossSelector`, and `CheckButtonGroup` widgets that share a compatible API.

#### Parameters

For more details on customization options, see the [customization guides](https://panel-material-ui.holoviz.org/customization/index.html).

##### Core

* **`disabled`** (bool): If True, the widget is not interactive.
* **`options`** (list or dict): The available options to choose from. Can be a list of strings or a dictionary mapping labels to values.
* **`value`** (list): The currently selected options.

##### Display

* **`inline`** (bool): Whether to lay out the options in a row (`inline=True`) or column (the default).
* **`label`** (str): The title displayed above the checkbox group.
* **`label_placement`** (`Literal["bottom", "start", "top", "end"]`): Placement of the option labels.
* **`loading`** (bool): If True, displays a loading spinner over the component.

##### Styling

- **`color`** (str): The color theme for the checkboxes.
- **`size`** (str, default="medium"): Controls the visual size/density of the checkboxes and their labels. One of "small", "medium", or "large".
- **`sx`** (dict): Component-level styling options.
- **`theme_config`** (dict): Theming configuration.

##### Aliases

For compatibility with Panel, some parameters have aliases:

- **`name`**: Alias for `label`

___

### Basic Usage

Create a checkbox group with a list of options. Users can select multiple items by checking the corresponding boxes:

```python
checkbox_group = pn.ui.CheckBoxGroup(
    label='Checkbox Group', value=['Apple', 'Pear'], options=['Apple', 'Banana', 'Pear', 'Strawberry'], inline=True
)

checkbox_group
```

The `value` parameter returns a list of the currently selected options:

```python
checkbox_group.value
```

### Dictionary Options

You can provide options as a dictionary where keys are the displayed labels and values are the actual option values:

```python
dict_group = pn.ui.CheckBoxGroup(
    label='Checkbox Group', value=['A', 'P'], options={'Apple': 'A', 'Banana': 'B', 'Pear': 'P', 'Strawberry': 'S'},
    inline=True,
)

dict_group
```

Let's observe how the `value` parameter reflects the selected dictionary values (not the labels):

```python
pn.pane.Str(dict_group.param.value)
```

### Orientation

Control the layout of checkboxes using the `inline` parameter:

```python
pn.ui.Column(
    pn.ui.CheckBoxGroup(label='Horizontal', value=['Apple', 'Pear'], options=['Apple', 'Banana', 'Pear', 'Strawberry'], inline=True),
    pn.ui.CheckBoxGroup(label='Vertical', value=['Apple', 'Pear'], options=['Apple', 'Banana', 'Pear', 'Strawberry'], inline=False)
)
```

## Label Placement

You may provide a `label_placement` as one of "bottom", "start", "top", "end":

```python
pn.ui.FlexBox(
    *(pn.ui.CheckBoxGroup(label=lp, label_placement=lp, inline=True, value=['Apple'], options=['Apple', 'Banana']) for lp in pn.ui.CheckBoxGroup.param.label_placement.objects)
)
```

### Color Options

Customize the appearance of checkboxes using the `color` parameter:

```python
pn.ui.FlexBox(
    *(pn.ui.CheckBoxGroup(label=color, color=color, inline=True, value=['Apple'], options=['Apple', 'Banana']) for color in pn.ui.CheckBoxGroup.param.color.objects)
)
```

### Size Options

Customize the size of the checkboxes using the `size` parameter:

```python
pn.ui.FlexBox(
    *(pn.ui.CheckBoxGroup(label=size, size=size, inline=True, value=['Apple'], options=['Apple', 'Banana']) for size in pn.ui.CheckBoxGroup.param.size.objects)
)
```

### Disabled and Loading

Like other widgets, the `CheckBoxGroup` can be disabled and/or show a loading indicator.

```python
pn.ui.CheckBoxGroup(
    label='Checkbox Group', value=['Apple', 'Pear'], options=['Apple', 'Banana', 'Pear', 'Strawberry'],
    disabled=True, loading=True
)
```

### Example: Interactive Pizza Order Form

Let's create a practical example showing how `CheckBoxGroup` can be used in a real application. This pizza ordering interface demonstrates real-time updates based on user selections:

```python
import panel as pn
import panel.ui

pn.extension()

toppings = pn.ui.CheckBoxGroup(
    label="Select your toppings:",
    options=['Pepperoni', 'Mushrooms', 'Bell Peppers', 'Onions', 'Olives', 'Extra Cheese'],
    value=['Pepperoni', 'Onions'],
    inline=True,
)

def create_order_summary(toppings):
    summary = f"## 🧺 Your Pizza Order\n\n"
    summary += f"• Toppings: {', '.join(toppings) if toppings else 'None'}\n"
    
    base_price = 12.99
    topping_price = len(toppings) * 1.50
    total = base_price + topping_price
    summary += f"\n**Total: ${total:.2f}**"
    
    return summary

order_summary = pn.bind(create_order_summary, toppings=toppings)

pn.ui.Column(
    "## 🍕 Pizza Order Form",
    toppings,
    "---",
    order_summary,
    width=800
)
```

### Icon Labels

Material icon tokens like `:material/zoom_out_map:` render as icons in labels and option labels.

```python
icon_options = {
    ":material/zoom_out_map: Full screen": "fullscreen",
    ":material/zoom_in: Zoom in": "zoom_in",
    ":material/zoom_out: Zoom out": "zoom_out",
}

pn.ui.CheckBoxGroup(
    label=":material/zoom_out_map: View",
    options=icon_options,
    value=["fullscreen", "zoom_in"],
    inline=True,
)
```

### API Reference

#### Parameters

```python
pn.ui.CheckBoxGroup(
    label='Checkbox Group', value=['Apple', 'Pear'], options=['Apple', 'Banana', 'Pear', 'Strawberry'],
).api(jslink=True)
```

### References

**Panel Documentation:**

- [How-to guides on interactivity](https://panel.holoviz.org/how_to/interactivity/index.html) - Learn how to add interactivity to your applications using widgets
- [Setting up callbacks and links](https://panel.holoviz.org/how_to/links/index.html) - Connect parameters between components and create reactive interfaces
- [Declarative UIs with Param](https://panel.holoviz.org/how_to/param/index.html) - Build parameter-driven applications

**Material UI CheckBox:**

- [Material UI CheckBox Reference](https://mui.com/material-ui/react-checkbox/#formgroup) - Complete documentation for the underlying Material UI component
