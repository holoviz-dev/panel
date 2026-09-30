# panel.io.document module

class panel.io.document.MockSessionContext(document: Document)
Bases: `SessionContext`

Attributes:
[destroyed](#panel.io.document.MockSessionContext.destroyed)
If `True`, the session has been discarded and
cannot be used.

[document](#panel.io.document.MockSessionContext.document)
The document associated with this session context.

**request**

**session**

Methods

|  |  |
|----|----|
| [with_locked_document](#panel.io.document.MockSessionContext.with_locked_document)(\*args) | Runs a function with the document lock held, passing the document to the function. |

property destroyed: bool
If `True`, the session has been discarded and
cannot be used.

A new session with the same ID could be created later but this instance
will not come back to life.

property document: Document
The document associated with this session context.

with_locked_document(\*args)
Runs a function with the document lock held, passing the document to the
function.

*Subclasses must implement this method.*

Args:
func (callable): function that takes a single parameter (the Document)
and returns `None` or a
`Future`

Returns:
a `Future` containing the result of the
function

class panel.io.document.Request(headers: 'dict', cookies: 'dict', arguments: 'dict')
Bases: `object`

panel.io.document.freeze_doc(doc: Document, model: HasProps, properties: dict\[str, t.Any\], force: bool = False)
Freezes the document model references if any of the properties are
themselves a model.

panel.io.document.hold(doc: Document \| None = None, policy: HoldPolicyType = 'combine', comm: Comm \| None = None, freeze: bool = False)
Context manager that holds events on a particular Document allowing them
all to be collected and dispatched when the context manager exits. This
allows multiple events on the same object to be combined if the policy
is set to ‘combine’.

Parameters:
**doc: Document**
The Bokeh Document to hold events on.

**policy: HoldPolicyType**
One of ‘combine’, ‘collect’ or None determining whether events setting
the same property are combined or accumulated to be dispatched when the
context manager exits.

**comm: Comm**
The Comm to dispatch events on when the context manager exits.

**freeze: bool**
**Experimental.** Whether to freeze the Document model references for
the duration of the hold. When True, defers expensive model graph
recomputation (`doc.models.recompute()`) until
the hold exits, which can significantly speed up batch updates that
modify many models. Safe to nest with the per-model
`freeze_doc` calls used internally, since
Bokeh’s freeze mechanism is reference-counted.

panel.io.document.immediate_dispatch(doc: Document \| None = None)
Context manager to trigger immediate dispatch of events triggered inside
the execution context even when Document events are currently on hold.

Parameters:
**doc: Document**
The document to dispatch events on (if None then state.curdoc is used).

panel.io.document.retrigger_events(doc: Document, events: list\[DocumentChangedEvent\])
Applies events that could not be processed previously.

panel.io.document.schedule_write_events(doc: Document, connections: Iterable\[ServerConnection\], events: list\[DocumentPatchedEvent\])
Queues events that cannot be written immediately, e.g. because the
socket is being written to or because we are not on the event loop
thread. The events are serialized by
`_dispatch_msgs` when they are actually
written.

panel.io.document.unlocked(policy: HoldPolicyType = 'combine') → Iterator
Context manager which unlocks a Document and dispatches
ModelChangedEvents triggered in the context body to all sockets on
current sessions.

Parameters:
**policy: Literal\[‘combine’ \| ‘collect’\]**
One of ‘combine’ or ‘collect’ determining whether events setting the
same property are combined or accumulated to be dispatched when the
context manager exits.

panel.io.document.with_lock(func: Callable) → Callable
Wrap a callback function to execute with a lock allowing the function to
modify bokeh models directly.

Parameters:
**func: callable**
The callable to wrap

Returns:
wrapper: callable
Function wrapped to execute without a Document lock.

panel.io.document.write_events(doc: Document, connections: Iterable\[ServerConnection\], events: list\[DocumentPatchedEvent\], run: bool = True) → list\[Future\]
Serializes the events into a single protocol message and writes it to
all the supplied connections.

A single message is shared between the connections since serializing a
patch marks the models it defines as synced on the Document, so
serializing per connection would make all but the first message
reference models the client was never sent.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
