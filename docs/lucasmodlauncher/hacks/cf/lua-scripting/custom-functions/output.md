---
title: Output
description: "Outputs text or binary data to a virtual file in memory which is then handed off to the game in place of the file it requested."
---

**This function should only be called in a [Path Handler](../path-handler-scripts.md) script.**

Outputs text or binary data to a virtual file in memory which is then handed off to the game in place of the file it requested.

# Syntax
```lua
Output( <string> )
```

* **string**: The string to output to the virtual file.

# Examples
```lua
-- Example that would be used in a PathHandler on an MFK script
Output([[
    LoadP3DFile("art\\cars\\famil_v.p3d");
]])
```

# Notes
No additional notes.

# Version History
## 1.23.9
Improved efficency of this function, particularly when calling it multiple times.

## Unknown Version
Added this function.