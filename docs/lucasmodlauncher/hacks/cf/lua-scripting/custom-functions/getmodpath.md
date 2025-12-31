---
title: GetModPath
description: "Returns the path to a mod within the Virtual File System."
---

Returns the path to a mod within the [Virtual File System](../../virtual-file-system.md).

# Syntax
```lua
GetModPath( [<mod_name>] )
```

* **mod_name**: Specify the InternalName of a mod whose path you want to get.
    * Optional, defaults to the mod that called the function.
    * This function always returns a path regardless of whether or not the specified mod name is valid or enabled.

# Examples
```lua
-- Get the current mod's path.
-- Returns "/Mods/CurrentMod"
local Path = GetModPath()

-- Get Donut Mod's path
local Path = GetModPath("DonutMod3")
```

# Notes
No additional notes.

# Version History
## Unknown Version
Added this function.