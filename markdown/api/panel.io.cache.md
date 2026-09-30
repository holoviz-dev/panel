# panel.io.cache module

Implements memoization for functions with arbitrary arguments

panel.io.cache.cache(func: Literal\[None\] = None, hash_funcs: dict\[type\[t.Any\], Callable\[\[t.Any\], bytes\]\] \| None = None, max_items: int \| None = None, policy: Literal\['FIFO', 'LRU', 'LFU'\] = 'LRU', ttl: float \| None = None, to_disk: bool = False, cache_path: str \| PathLike \| None = None, per_session: bool = False, approximate: bool = True) → Callable\[\[Callable\[\_P, \_R\]\], \_CachedFunc\[Callable\[\_P, \_R\]\]\]\
panel.io.cache.cache(func: Callable\[\_P, \_R\], hash_funcs: dict\[type\[t.Any\], Callable\[\[t.Any\], bytes\]\] \| None = None, max_items: int \| None = None, policy: Literal\['FIFO', 'LRU', 'LFU'\] = 'LRU', ttl: float \| None = None, to_disk: bool = False, cache_path: str \| PathLike \| None = None, per_session: bool = False, approximate: bool = True) → \_CachedFunc\[Callable\[\_P, \_R\]\]
Memoizes functions for a user session. Can be used as function
annotation or just directly.

For global caching across user sessions use pn.state.as_cached.

Cached results are stored and handed out as they are, i.e. every hit
returns the very same object. Mutating a returned value therefore
changes what later hits see, so treat results as read-only or copy them
before modifying.

Arguments are hashed by their contents on every call, so a cache hit on
a large DataFrame or array still costs a pass over the data. By default
inputs above 100k rows (or elements) are hashed from a fixed
pseudo-random sample of 100k rows, which makes the hash approximate: a
difference confined to the rows that were not sampled is invisible and
returns the previously cached result. Set
`approximate=False` to hash all the data, or
pass a `hash_funcs` entry for the type to hash
such inputs some other way, e.g. by a version or timestamp you maintain
yourself.

Arguments that are mutated in place between calls are also invisible
once the result has been cached, since the mutated object may hash the
same as the object that was cached.

Parameters:
**func: callable**
The function to cache.

**hash_funcs: dict or None**
A dictionary mapping from a type to a function which returns a hash for
an object of that type. If provided this will override the default
hashing function provided by Panel.

**max_items: int or None**
The maximum items to keep in the cache. Default is None, which does not
limit number of items stored in the cache.

**policy: str**
A caching policy when max_items is set, must be one of:
- FIFO: First in - First out

- LRU: Least recently used

- LFU: Least frequently used

**ttl: float or None**
The number of seconds to keep an item in the cache, or None if the cache
should not expire. The default is None.

**to_disk: bool**
Whether to cache to disk using diskcache.

**cache_path: str**
Directory to cache to on disk (if not provided default will be inherited
from config.cache_path).

**per_session: bool**
Whether to cache data only for the current session.

**approximate: bool**
Whether DataFrames, Series and arrays above 100k rows (or elements) may
be hashed from a sample of their contents, which is cheaper but can
return the result cached for a different input. Set to False to hash all
the data.

panel.io.cache.compute_hash(func, hash_funcs, args, kwargs, approximate=True)
Computes a hash given a function and its arguments.

Parameters:
**func: callable**
The function to cache.

**hash_funcs: dict**
A dictionary of custom hash functions indexed by type

**args: tuple**
Arguments to hash

**kwargs: dict**
Keyword arguments to hash

**approximate: bool**
Whether DataFrames, Series and arrays above 100k rows (or elements) may
be hashed from a sample of their contents.

panel.io.cache.is_equal(value, other) → bool
Returns True if value and other are equal

Supports complex values like DataFrames

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
