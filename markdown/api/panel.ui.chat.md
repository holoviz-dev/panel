# panel.ui.chat package

## Module contents

The Material UI chat components.

class panel.ui.chat.ChatAreaInput(\*, accept, actions, disabled_enter, enable_upload, enter_sends, footer_objects, value_uploaded, views, auto_grow, cols, enter_pressed, max_rows, resizable, rows, max_length, placeholder, size, color, error_state, helper_text, variant, attached, description, disabled, dark_theme, sx, theme_config, use_shadow_dom, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, chunk_size, max_file_size, max_total_file_size, uploaded_label, name)
Bases: [TextAreaInput](panel.ui.widgets.md#panel.ui.widgets.TextAreaInput),
`_FileUploadArea`

The ChatAreaInput allows entering any multiline string using a text
input box, with the ability to press enter to submit the message.

Unlike TextAreaInput, the ChatAreaInput defaults to auto_grow=True and
max_rows=10, and the value is not synced to the server until the enter
key is pressed so bind on value_input if you need to access the existing
value.

Lines are joined with the newline character n.

References:

- [https://panel-material-ui.holoviz.org/reference/chat/ChatAreaInput.html](https://panel-material-ui.holoviz.org/reference/chat/ChatAreaInput.html)

- [https://panel.holoviz.org/reference/chat/ChatAreaInput.html](https://panel.holoviz.org/reference/chat/ChatAreaInput.html)

Example:

\>\>\> ChatAreaInput(max_rows=10)\

Methods

|  |  |
|----|----|
| [focus](#panel.ui.chat.ChatAreaInput.focus)() | Focus the input element. |
| [on_action](#panel.ui.chat.ChatAreaInput.on_action)(name, callback) | Registers a callback that is invoked when an action triggered. |
| [remove_on_action](#panel.ui.chat.ChatAreaInput.remove_on_action)(name, callback) | Removes a callback that was registered with on_action. |
| [sync](#panel.ui.chat.ChatAreaInput.sync)() | Syncs currently uploaded files to the server without requiring the user to press enter or click submit. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> `panel_material_ui.widgets.input._FileUploadArea`:
> chunk_size, max_file_size, max_total_file_size, uploaded_label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, height, min_width,
> min_height, max_width, max_height, styles, stylesheets, tags,
> width_policy, height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.custom.ReactComponent"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.custom.ReactComponent](panel.custom.md#panel.custom.ReactComponent):
> use_shadow_dom
>
> [class="reference internal"
> title="panel_material_ui.base.MaterialComponent"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.base.MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent):
> dark_theme, theme_config, sx
>
> [class="reference internal"
> title="panel_material_ui.widgets.base.MaterialWidget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets.base.MaterialWidget](panel.ui.base.md#panel.ui.base.MaterialWidget):
> label, margin, width, attached, description, disabled
>
> `panel_material_ui.widgets.input.MaterialInputWidget`:
> color, error_state, helper_text, variant
>
> `panel_material_ui.widgets.input._TextInputBase`:
> value, size, value_input
>
> [class="reference internal"
> title="panel_material_ui.widgets.input.TextAreaInput"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.widgets. input .TextAreaInput](panel.ui.widgets.md#panel.ui.widgets.TextAreaInput):
> cols, resizable
>
>

`loading`` ``=`` ``Boolean(allow_refs=True,`` ``default=False,`` ``label='Loading')`
If True displays a loading spinner on top of the component.

`max_length`` ``=`` ``Integer(default=50000,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Max`` ``length')`
Max count of characters in the input field.

`placeholder`` ``=`` ``String(default='Ask`` ``anything...',`` ``label='Placeholder')`
Placeholder for empty input field.

`auto_grow`` ``=`` ``Boolean(default=True,`` ``label='Auto`` ``grow')`
Whether the text area should automatically grow vertically to
accommodate the current text.

`max_rows`` ``=`` ``Integer(default=10,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Max`` ``rows')`
When combined with auto_grow this determines the maximum number of rows
the input area can grow.

`rows`` ``=`` ``Integer(default=1,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Rows')`
Number of rows in the text input field.

`enter_pressed`` ``=`` ``Event(default=False,`` ``label='Enter`` ``pressed')`
If True, pressing the Enter key sends the message, if False it is sent
by pressing the Ctrl+Enter.

`accept`` ``=`` ``String(allow_None=True,`` ``label='Accept')`
A comma separated string of file extensions (with dots) or MIME types
that should be accepted for upload. Examples: ‘.csv,.json,.txt’ or
‘text/csv,application/json’.

`actions`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={},`` ``label='Actions')`
A dictionary of actions that can be invoked via the speed dial to the
left of input area. The actions should be defined as a dictionary
indexed by the name of the action mapping to values that themselves are
dictionaries containing an icon. Users can define callbacks by
registering callbacks using the on_action method.

`disabled_enter`` ``=`` ``Boolean(default=False,`` ``label='Disabled`` ``enter')`
If True, disables sending the message by pressing the enter_sends key.

`enable_upload`` ``=`` ``Boolean(default=True,`` ``label='Enable`` ``upload')`
If True, enables uploading of files.

`enter_sends`` ``=`` ``Boolean(default=True,`` ``label='Enter`` ``sends')`
If True, pressing the Enter key sends the message, if False it is sent
by pressing the Ctrl+Enter.

`pending_uploads`` ``=`` ``Integer(constant=True,`` ``default=0,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Pending`` ``uploads',`` ``readonly=True)`
The number of files currently queued for upload but not yet transferred.
This is updated automatically when files are added or removed in the UI.

`value_uploaded`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={},`` ``label='Value`` ``uploaded')`
Dictionary containing raw file data keyed by filename after user sends
uploads. Each entry contains mime_type, value (bytes), and size.

`views`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Views')`
Views generated from uploaded files.

`footer_objects`` ``=`` ``Children(bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'panel.viewable.Viewable'>,`` ``label='Footer`` ``objects')`
A list of panel objects to display in the footer area below the input.

focus()
Focus the input element.

on_action(name: str, callback: Callable)
Registers a callback that is invoked when an action triggered.

Parameters:
**name: str**
The name of the action to register the callback for.

**callback: callable**
The callback to invoke when the action is triggered.

remove_on_action(name: str, callback: Callable)
Removes a callback that was registered with on_action.

Parameters:
**name: str**
The name of the action to register the callback for.

**callback: callable**
The callback to invoke when the action is triggered.

sync()
Syncs currently uploaded files to the server without requiring the user
to press enter or click submit. This allows programmatic control over
when file uploads are processed.

This method is asynchronous - it sends a message to the frontend to
initiate the sync and returns immediately. To access the uploaded file
data, watch for changes to the value_uploaded parameter.

class panel.ui.chat.ChatFeed(\*objects, **params)
Bases: [ChatFeed](panel.chat.feed.md#panel.chat.feed.ChatFeed)

A ChatFeed holds a list of ChatMessage objects and provides convenient
APIs. to interact with them.

This includes methods to: - Send (append) messages to the chat log. -
Stream tokens to the latest ChatMessage in the chat log. - Execute
callbacks when a user sends a message. - Undo a number of sent
ChatMessage objects. - Clear the chat log of all ChatMessage objects.

References:

- [https://panel-material-ui.holoviz.org/reference/chat/ChatFeed.html](https://panel-material-ui.holoviz.org/reference/chat/ChatFeed.html)

- [https://panel.holoviz.org/reference/chat/ChatFeed.html](https://panel.holoviz.org/reference/chat/ChatFeed.html)

Example:

\>\>\> async def say_welcome(contents, user, instance):\
\>\>\>    yield "Welcome!"\
\>\>\>    yield "Glad you're here!"\

\>\>\> chat_feed = ChatFeed(callback=say_welcome, header="Welcome Feed")\
\>\>\> chat_feed.send("Hello World!", user="New User", avatar="😊")\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, height, min_width,
> min_height, max_width, max_height, styles, stylesheets, tags, width,
> width_policy, height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.layout.base.ListPanel"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.ListPanel](panel.layout.base.md#panel.layout.base.ListPanel):
> scroll
>
> [class="reference internal" title="panel.chat.feed.ChatFeed"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.chat.feed.ChatFeed](panel.chat.feed.md#panel.chat.feed.ChatFeed):
> margin, objects, adaptive, auto_scroll_limit, callback,
> callback_exception, callback_user, callback_avatar, edit_callback,
> card_params, collapsible, disabled, message_params, header, help_text,
> load_buffer, placeholder_text, placeholder_params,
> placeholder_threshold, post_hook, renderers, scroll_button_threshold,
> show_activity_dot, view_latest, \_placeholder, \_callback_state,
> \_prompt_trigger, \_callback_trigger, \_disabled_stack
>
>

`dark_theme`` ``=`` ``Boolean(default=False,`` ``label='Dark`` ``theme')`
Whether to use dark theme. If not specified, will default to Panel’s
global theme setting.

`theme_config`` ``=`` ``Dict(allow_None=True,`` ``class_=<class`` ``'dict'>,`` ``label='Theme`` ``config',`` ``nested_refs=True)`
Options to configure the ThemeProvider. See
[https://mui.com/material-ui/customization/theme-overview/](https://mui.com/material-ui/customization/theme-overview/)
for more information.

`sx`` ``=`` ``Dict(allow_None=True,`` ``class_=<class`` ``'dict'>,`` ``label='Sx')`
A dictionary of CSS styles to apply to the component. The keys are the
CSS class names and the values are the styles. The CSS class names are
generated by the component and can be found in the component’s
documentation.

class panel.ui.chat.ChatInterface(\*, input_params, on_submit, dark_theme, sx, theme_config, \_button_data, \_buttons, \_input_container, \_input_layout, \_widgets, auto_send_types, avatar, button_properties, reset_on_send, show_button_name, show_button_tooltips, show_clear, show_rerun, show_send, show_stop, show_undo, user, widgets, \_callback_state, \_callback_trigger, \_disabled_stack, \_placeholder, \_prompt_trigger, adaptive, auto_scroll_limit, callback, callback_avatar, callback_exception, callback_user, card_params, disabled, edit_callback, header, help_text, load_buffer, message_params, placeholder_params, placeholder_text, placeholder_threshold, post_hook, renderers, scroll_button_threshold, show_activity_dot, view_latest, scroll, objects, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, name)
Bases: [ChatFeed](#panel.ui.chat.ChatFeed),
[ChatInterface](panel.chat.interface.md#panel.chat.interface.ChatInterface)

A chat interface that uses Material UI components.

References:

- [https://panel-material-ui.holoviz.org/reference/chat/ChatInterface.html](https://panel-material-ui.holoviz.org/reference/chat/ChatInterface.html)

- [https://panel.holoviz.org/reference/chat/ChatInterface.html](https://panel.holoviz.org/reference/chat/ChatInterface.html)

Example:

\>\>\> ChatInterface().servable()\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, css_classes, design, height, min_width,
> min_height, max_width, max_height, styles, stylesheets, tags, width,
> width_policy, height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.layout.base.ListPanel"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.ListPanel](panel.layout.base.md#panel.layout.base.ListPanel):
> scroll
>
> [class="reference internal" title="panel.chat.feed.ChatFeed"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.chat.feed.ChatFeed](panel.chat.feed.md#panel.chat.feed.ChatFeed):
> margin, objects, adaptive, auto_scroll_limit, callback,
> callback_exception, callback_user, callback_avatar, edit_callback,
> card_params, collapsible, disabled, message_params, header, help_text,
> load_buffer, placeholder_text, placeholder_params,
> placeholder_threshold, post_hook, renderers, scroll_button_threshold,
> show_activity_dot, view_latest, \_placeholder, \_callback_state,
> \_prompt_trigger, \_callback_trigger, \_disabled_stack
>
> [class="reference internal"
> title="panel.chat.interface.ChatInterface"> class="sourceCode python xref py py-class docutils literal notranslate">panel.chat.interface.ChatInterface](panel.chat.interface.md#panel.chat.interface.ChatInterface):
> auto_send_types, avatar, reset_on_send, show_send, show_stop,
> show_rerun, show_undo, show_clear, show_button_name,
> show_button_tooltips, user, button_properties, \_widgets,
> \_input_container, \_input_layout, \_button_data, \_buttons
>
> [title="panel_material_ui.chat.feed.ChatFeed"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.chat.feed.ChatFeed](#panel.ui.chat.ChatFeed):
> dark_theme, theme_config, sx
>
>

`widgets`` ``=`` ``Parameter(allow_None=True,`` ``constant=True,`` ``label='Widgets')`
Not supported by panel-material-ui ChatInterface.

`input_params`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={},`` ``label='Input`` ``params')`
Additional parameters to pass to the ChatAreaInput widget. Supported
keys include any ChatAreaInput param, e.g.
`placeholder`,
`enable_upload`,
`max_rows`, `rows`.
Updates are applied dynamically after initialization.

`on_submit`` ``=`` ``Callable(allow_None=True,`` ``label='On`` ``submit')`
Callback to invoke when the send button or enter is pressed; should
accept an event and instance as args. If unspecified, the default
behavior is to send a Column containing the input text and views. This
only affects the user-facing input, and does not affect the send method.

class panel.ui.chat.ChatMessage(object=None, **params)
Bases: [MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent),
[ChatMessage](panel.chat.message.md#panel.chat.message.ChatMessage)

Renders another component as a chat message with an associated user and
avatar with support for various content types.

This widget provides a structured view of chat messages, including
features like:

- Displaying user avatars, which can be text, emoji, or images.

- Showing the user’s name.

- Displaying the message timestamp in a customizable format.

- Associating reactions with messages and mapping them to icons.

- Rendering various content types including text, images, audio, video,
  and more.

References:

- [https://panel-material-ui.holoviz.org/reference/chat/ChatMessage.html](https://panel-material-ui.holoviz.org/reference/chat/ChatMessage.html)

- [https://panel.holoviz.org/reference/chat/ChatMessage.html](https://panel.holoviz.org/reference/chat/ChatMessage.html)

Example:

\>\>\> ChatMessage(object="Hello world!", user="New User", avatar="😊")\

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, design, height, min_width, min_height,
> max_height, styles, stylesheets, tags, width, width_policy,
> height_policy, sizing_mode, visible
>
> [class="reference internal" title="panel.pane.base.PaneBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.pane.base.PaneBase](panel.pane.base.md#panel.pane.base.PaneBase):
> margin
>
> [class="reference internal" title="panel.chat.message.ChatMessage"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.chat.message.ChatMessage](panel.chat.message.md#panel.chat.message.ChatMessage):
> max_width, object, avatar_lookup, edited, footer_objects,
> header_objects, reactions, reaction_icons, timestamp,
> timestamp_format, timestamp_tz, show_avatar, show_edit_icon,
> show_user, show_timestamp, show_reaction_icons, show_copy_icon,
> show_activity_dot, renderers, user
>
> [class="reference internal" title="panel.custom.ReactComponent"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.custom.ReactComponent](panel.custom.md#panel.custom.ReactComponent):
> use_shadow_dom
>
> [class="reference internal"
> title="panel_material_ui.base.MaterialComponent"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.base.MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent):
> loading, dark_theme, theme_config, sx
>
>

`css_classes`` ``=`` ``List(allow_refs=True,`` ``bounds=(0,`` ``None),`` ``default=[],`` ``item_type=<class`` ``'str'>,`` ``label='Css`` ``classes',`` ``nested_refs=True)`
The CSS classes to apply to the widget.

`default_layout`` ``=`` ``ClassSelector(allow_None=True,`` ``class_=<class`` ``'panel.layout.base.Panel'>,`` ``default=<class`` ``'panel.layout.base.Row'>,`` ``label='Default`` ``layout')`
Defines the layout the model(s) returned by the pane will be placed in.

`avatar`` ``=`` ``ClassSelector(class_=(<class`` ``'str'>,`` ``<class`` ``'_io.BytesIO'>,`` ``<class`` ``'bytes'>,`` ``<class`` ``'panel.pane.image.ImageBase'>,`` ``<class`` ``'dict'>),`` ``default='',`` ``label='Avatar')`
The avatar to use for the user. Can be a single character text, an
emoji, or anything supported by pn.pane.Image. If not set, checks if the
user is available in the default_avatars mapping; else uses the first
character of the name.

`default_avatars`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={'system':`` ``'⚙️',`` ``'client':`` ``'🧑',`` ``'customer':`` ``'🧑',`` ``'employee':`` ``'🧑',`` ``'human':`` ``'🧑',`` ``'person':`` ``'🧑',`` ``'user':`` ``'🧑',`` ``'agent':`` ``'🤖',`` ``'ai':`` ``'🤖',`` ``'assistant':`` ``'🤖',`` ``'bot':`` ``'🤖',`` ``'chatbot':`` ``'🤖',`` ``'machine':`` ``'🤖',`` ``'robot':`` ``'🤖',`` ``'exception':`` ``'❌',`` ``'error':`` ``'❌',`` ``'help':`` ``'❓',`` ``'input':`` ``'❗',`` ``'adult':`` ``'🧑',`` ``'baby':`` ``'👶',`` ``'boy':`` ``'👦',`` ``'child':`` ``'🧒',`` ``'girl':`` ``'👧',`` ``'man':`` ``'👨',`` ``'woman':`` ``'👩',`` ``'chatgpt':`` ``'{dist_path}assets/logo/gpt-3.svg',`` ``'gpt3':`` ``'{dist_path}assets/logo/gpt-3.svg',`` ``'gpt4':`` ``'{dist_path}assets/logo/gpt-4.svg',`` ``'dalle':`` ``'{dist_path}assets/logo/gpt-4.svg',`` ``'openai':`` ``'{dist_path}assets/logo/gpt-4.svg',`` ``'huggingface':`` ``'🤗',`` ``'calculator':`` ``'🧮',`` ``'langchain':`` ``'🦜',`` ``'retriever':`` ``'📄',`` ``'tool':`` ``'🛠️',`` ``'translator':`` ``'🌐',`` ``'wolfram':`` ``'{dist_path}assets/logo/wolfram.svg',`` ``'wolfram`` ``alpha':`` ``'{dist_path}assets/logo/wolfram.svg',`` ``'llama':`` ``'🦙',`` ``'llama2':`` ``'🐪',`` ``'plot':`` ``'📊',`` ``'lumen':`` ``'{dist_path}assets/logo/lumen.svg',`` ``'holoviews':`` ``'{dist_path}assets/logo/holoviews.svg',`` ``'hvplot':`` ``'{dist_path}assets/logo/hvplot.svg',`` ``'panel':`` ``'{dist_path}images/icon-vector.svg'},`` ``label='Default`` ``avatars')`
A default mapping of user names to their corresponding avatars to use
when the user is specified but the avatar is. You can modify, but not
replace the dictionary.

`elevation`` ``=`` ``Integer(default=2,`` ``inclusive_bounds=(True,`` ``True),`` ``label='Elevation')`
The elevation of the message.

`placement`` ``=`` ``Selector(default='left',`` ``label='Placement',`` ``names={},`` ``objects=['left',`` ``'right'])`
The placement of the message.

`_internal_state`` ``=`` ``ClassSelector(class_=<class`` ``'panel_material_ui.chat.message.MessageState'>,`` ``default=MessageState(avatar=None,`` ``name='MessageState00116',`` ``timestamp=''),`` ``label='`` ``internal`` ``state')`

`_object_panel`` ``=`` ``Child(allow_None=True,`` ``class_=<class`` ``'panel.viewable.Viewable'>,`` ``label='`` ``object`` ``panel')`

default_layout
alias of [Row](panel.layout.base.md#panel.layout.base.Row)

class panel.ui.chat.ChatReactionIcons(\*, active_icons, default_layout, options, disabled, loading, align, aspect_ratio, css_classes, design, height, height_policy, margin, max_height, max_width, min_height, min_width, sizing_mode, styles, stylesheets, tags, visible, width, width_policy, label, value, name)
Bases:
[CompositeWidget](panel.widgets.base.md#panel.widgets.base.CompositeWidget)

A widget to display reaction icons that can be clicked on.

Parameters:
value : List
The selected reactions.

options : Dict
A key-value pair of reaction values and their corresponding tabler icon
names found on [https://tabler.io/icons](https://tabler.io/icons).

active_icons : Dict
The mapping of reactions to their corresponding active icon names; if
not set, the active icon name will default to its “filled” version.

**Reference: https://panel.holoviz.org/reference/chat/ChatReactionIcons.html**

**:Example:**

**\>\>\> ChatReactionIcons(value=\[“like”\], options={“like”: “thumb-up”, “dislike”: “thumb-down”})**

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> [class="reference internal" title="panel.widgets.base.WidgetBase"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.WidgetBase](panel.widgets.base.md#panel.widgets.base.WidgetBase):
> label
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, design, min_width, min_height, max_width,
> max_height, styles, stylesheets, tags, width_policy, height_policy,
> sizing_mode, visible
>
> [class="reference internal" title="panel.viewable.Viewable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Viewable](panel.viewable.md#panel.viewable.Viewable):
> loading
>
> [class="reference internal" title="panel.widgets.base.Widget"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.widgets.base.Widget](panel.widgets.base.md#panel.widgets.base.Widget):
> height, width, disabled
>
>

`value`` ``=`` ``List(bounds=(0,`` ``None),`` ``default=[],`` ``label='Value')`
The active reactions.

`css_classes`` ``=`` ``List(allow_refs=True,`` ``bounds=(0,`` ``None),`` ``default=['reaction-icons'],`` ``item_type=<class`` ``'str'>,`` ``label='Css`` ``classes',`` ``nested_refs=True)`
The CSS classes of the widget.

`margin`` ``=`` ``Margin(allow_None=True,`` ``allow_refs=True,`` ``default=0,`` ``label='Margin')`
Allows to create additional space around the component. May be specified
as a two-tuple of the form (vertical, horizontal) or a four-tuple (top,
right, bottom, left).

`active_icons`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={},`` ``label='Active`` ``icons')`
The mapping of reactions to their corresponding active icon names. If
not set, the active icon name will default to its “filled” version.

`options`` ``=`` ``Dict(class_=<class`` ``'dict'>,`` ``default={'favorite':`` ``'heart'},`` ``label='Options')`
A key-value pair of reaction values and their corresponding tabler icon
names found on [https://tabler.io/icons](https://tabler.io/icons).

`default_layout`` ``=`` ``ClassSelector(class_=<class`` ``'panel.layout.base.Panel'>,`` ``default=<class`` ``'panel.layout.base.Column'>,`` ``label='Default`` ``layout')`
The layout to use for the icons. Defaults to Column, which stacks the
icons vertically.

default_layout
alias of [Column](panel.layout.base.md#panel.layout.base.Column)

class panel.ui.chat.ChatStep(\*objects, **params)
Bases: [Card](panel.ui.layout.md#panel.ui.layout.Card),
[ChatStep](panel.chat.step.md#panel.chat.step.ChatStep)

A component that makes it easy to provide status updates and the ability
to stream updates to both the output(s) and the title.

References:

- [https://panel-material-ui.holoviz.org/reference/chat/ChatStep.html](https://panel-material-ui.holoviz.org/reference/chat/ChatStep.html)

- [https://panel.holoviz.org/reference/chat/ChatStep.html](https://panel.holoviz.org/reference/chat/ChatStep.html)

Example:

\>\>\> ChatStep("Hello world!", title="Running calculation...', status="running")\

Methods

|  |  |
|----|----|
| [stream](#panel.ui.chat.ChatStep.stream)(token\[, replace\]) | Stream a token to the last available string-like object. |

**Parameter Definitions**

------------------------------------------------------------------------

Parameters inherited from:

>
>
> `panel_material_ui.layout.base.PaperMixin`:
> elevation, raised, square, variant
>
> [class="reference internal" title="panel.viewable.Layoutable"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.viewable.Layoutable](panel.viewable.md#panel.viewable.Layoutable):
> align, aspect_ratio, design, height, min_width, min_height, max_width,
> max_height, styles, stylesheets, tags, width, width_policy,
> height_policy, visible
>
> [class="reference internal" title="panel.layout.base.ListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.ListLike](panel.layout.base.md#panel.layout.base.ListLike):
> objects
>
> [class="reference internal" title="panel.layout.base.ListPanel"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.ListPanel](panel.layout.base.md#panel.layout.base.ListPanel):
> scroll
>
> [class="reference internal" title="panel.layout.base.Column"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.base.Column](panel.layout.base.md#panel.layout.base.Column):
> auto_scroll_limit, scroll_button_threshold, scroll_position,
> view_latest
>
> [class="reference internal" title="panel.layout.card.Card"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.layout.card.Card](panel.layout.card.md#panel.layout.card.Card):
> css_classes, active_header_background, button_css_classes
>
> [class="reference internal" title="panel.chat.step.ChatStep"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.chat.step.ChatStep](panel.chat.step.md#panel.chat.step.ChatStep):
> collapsed_on_success, context_exception, default_badges,
> default_title, failed_title, pending_title, running_title, status,
> success_title
>
> [class="reference internal" title="panel.custom.ReactComponent"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel.custom.ReactComponent](panel.custom.md#panel.custom.ReactComponent):
> use_shadow_dom
>
> [class="reference internal"
> title="panel_material_ui.base.MaterialComponent"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.base.MaterialComponent](panel.ui.base.md#panel.ui.base.MaterialComponent):
> loading, dark_theme, theme_config, sx
>
> [class="reference internal"
> title="panel_material_ui.layout.base.MaterialNamedListLike"> class="pre"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.MaterialNamedListLike](panel.ui.base.md#panel.ui.base.MaterialNamedListLike):
> \_names, \_headers
>
> [class="reference internal"
> title="panel_material_ui.layout.base.Card"> class="sourceCode python xref py py-class docutils literal notranslate">panel_material_ui.layout.base.Card](panel.ui.layout.md#panel.ui.layout.Card):
> collapsed, collapsible, header, header_background, header_color,
> header_css_classes, hide_header, outlined, title, title_css_classes,
> title_variant
>
>

`margin`` ``=`` ``Margin(allow_None=True,`` ``allow_refs=True,`` ``default=(5,`` ``0,`` ``0,`` ``0),`` ``label='Margin')`
The margin of the layout.

`sizing_mode`` ``=`` ``Selector(allow_refs=True,`` ``default='stretch_width',`` ``label='Sizing`` ``mode',`` ``names={},`` ``objects=['fixed',`` ``'stretch_width',`` ``'stretch_height',`` ``'stretch_both',`` ``'scale_width',`` ``'scale_height',`` ``'scale_both',`` ``None])`
How the component should size itself. This is a high-level setting for
maintaining width and height of the component. To gain more fine grained
control over sizing, use `width_policy`,
`height_policy` and
`aspect_ratio` instead (those take precedence
over `sizing_mode`).
`"fixed"` Component is not responsive. It will
retain its original width and height regardless of any subsequent
browser window resize events. `"stretch_width"`
Component will responsively resize to stretch to the available width,
without maintaining any aspect ratio. The height of the component
depends on the type of the component and may be fixed or fit to
component’s contents. `"stretch_height"`
Component will responsively resize to stretch to the available height,
without maintaining any aspect ratio. The width of the component depends
on the type of the component and may be fixed or fit to component’s
contents. `"stretch_both"` Component is
completely responsive, independently in width and height, and will
occupy all the available horizontal and vertical space, even if this
changes the aspect ratio of the component.
`"scale_width"` Component will responsively
resize to stretch to the available width, while maintaining the original
or provided aspect ratio. `"scale_height"`
Component will responsively resize to stretch to the available height,
while maintaining the original or provided aspect ratio.
`"scale_both"` Component will responsively
resize to both the available width and height, while maintaining the
original or provided aspect ratio.

stream(token: str \| None, replace: bool = False)
Stream a token to the last available string-like object.

Parameters:
token : str
The token to stream.

replace : bool
Whether to replace the existing text.

Returns:
Viewable
The updated message pane.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
