# Difference between exit() and sys.exit() in Python

A answer from Stack Overflow:
> `exit` is a helper for the interactive shell - `sys.exit` is intended for use in programs.

> > The `site` module (which is imported automatically during startup, except if the `-S` command-line option is given) adds several constants to the built-in namespace (e.g. `exit`). **They are useful for the interactive interpreter shell and should not be used in programs**.

[The answer](https://stackoverflow.com/questions/6501121/difference-between-exit-and-sys-exit-in-python/6501134#6501134)