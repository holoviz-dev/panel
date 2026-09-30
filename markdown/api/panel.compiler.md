# panel.compiler module

Utilities for building custom models included in panel.

panel.compiler.bundle_licenses(verbose=False, download_list=None)
Bundles the license of every third-party library collected so far.

Has to run after the other bundle\_\* functions, since the set of
licenses is derived from the urls they collected.

panel.compiler.prune_unminified_duplicates(verbose=False)
Drops every bundled file that also has a minified build alongside it.

Runs over the finished bundle rather than over each archive because the
two builds do not always come from the same place: reveal.js publishes
only `reveal.css` in its tarball, and Panel
fetches `reveal.min.css` from the CDN because
that is the one the template asks for.

[![Support us with a star on
GitHub](https://img.shields.io/github/stars/holoviz/panel?style=social&label=Star%20on%20%20GitHub%E2%AD%90)](https://github.com/holoviz/panel)

On this page
