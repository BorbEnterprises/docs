---
title: Redirect
description: "Redirect the file being requested to a different path."
---

**This function should only be called in a [Path Handler](../path-handler-scripts.md) script.**

Redirect the file being requested to a different path.

# Syntax
```lua
Redirect( <path> )
```

* **path**: The path to redirect this file to.

# Examples
```lua
-- Example redirection to a random file in the Mod's Resources folder.
local FilePath = GetModPath() .. "/Resources/example/"

local Files = {"example.p3d","example2.p3d","example3.p3d"}

Redirect(FilePath .. Files[math.random(1, #Files)])
```

# Notes
No additional notes.

# Version History
## Unknown Version
Added this function.