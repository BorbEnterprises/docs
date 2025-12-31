---
title: GetPath
description: "Returns the path of the file being requested."
---

**This function should only be called in a [Path Handler](../path-handler-scripts.md) script.**

Returns the path of the file being requested.

# Syntax
```lua
GetPath()
```

# Examples
```lua
local CurrentPath = GetPath()

if ComparePaths(CurrentPath, "scripts\\missions\\rewards.mfk") then
    -- Do something based on it being the rewards file.
else
    -- Do something else, nothing probably with this example
end
```

# Notes
No additional notes.

# History
## Unknown Version
Added this function.