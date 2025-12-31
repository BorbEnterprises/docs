---
title: GetMainMod
description: "Returns the InternalName of the current main mod."
---

Returns the InternalName of the current main mod.

If no main mod is enabled, this will return `nil`.

# Syntax
```lua
GetMainMod()
```

# Examples
```lua
local CurrentMainMod = GetMainMod()

if CurrentMainMod == "DonutMod3" then
    -- Donut Mod specific code.
else
    -- Whatever else you want.
end
```

# Notes
No additional notes.

# History
## 1.19
Added this function.