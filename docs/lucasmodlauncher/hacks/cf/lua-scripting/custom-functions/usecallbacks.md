---
title: UseCallbacks
description: "Builds a file as the game requests it using callback functions."
status:
    class: "wip"
---

**This function should only be called in a [Path Handler](../path-handler-scripts.md) script.**

Builds a file as the game requests it using callback functions.

# Syntax
```lua
UseCallbacks( <length>, <read_callback>, <close_callback>)
```

* **length**: The filesize of the file in bytes.
* **read_callback**: This callback function will get called each time the game tries to read from the file.
* **close_callback**: This callback gets called when the game is done with the file.

# Examples
TODO

# Version History
## 1.24
Fixed a major issue where Lua functions that are only supposed to work when handling a path (`Output`, `Redirect`, `GetPath`, `IsWriting` and `UseCallbacks`) could be called in a `UseCallbacks` callback but would not work properly. Now they cannot be called in this case.

## 1.19
Added this function.