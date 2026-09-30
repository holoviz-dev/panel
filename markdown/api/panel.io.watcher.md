# panel.io.watcher module

Shared file watching for the autoreload development loop.

Components that render from the same file, e.g. every component compiled
into a shared ESM bundle, would otherwise each start their own watcher
task. This module hands out one watcher per path and notifies all its
subscribers when the file changes.

class panel.io.watcher.PathWatcher(path: Path)
Bases: `object`

Watches a single path on behalf of any number of subscribers.

Subscribers are held weakly, so subscribing does not keep a component
alive; each is notified by calling the method it subscribed with.

Attributes:
**running**

Methods

|  |  |
|----|----|
| [subscribe](#panel.io.watcher.PathWatcher.subscribe)(obj, method) | Subscribes an object to changes of the watched path. |
| [unsubscribe](#panel.io.watcher.PathWatcher.unsubscribe)(obj\[, method\]) | Unsubscribes an object, either from a single method or entirely. |

subscribe(obj: Any, method: str) → None
Subscribes an object to changes of the watched path.

Parameters:
**obj: Any**
The object to notify, held weakly.

**method: str**
Name of the method to invoke on the object.

unsubscribe(obj: Any, method: str \| None = None) → None
Unsubscribes an object, either from a single method or entirely.

panel.io.watcher.current_path_watchers() → dict\[Path, PathWatcher\]
Returns the watchers that have been created so far.

panel.io.watcher.get_path_watcher(path: str \| PathLike) → PathWatcher
Returns the process-wide watcher for the given path, creating it on
first use.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
