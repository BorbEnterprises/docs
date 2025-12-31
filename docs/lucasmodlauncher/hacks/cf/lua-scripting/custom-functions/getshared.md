---
title: GetShared
description: "Returns a table that is shared by all mods."
authors: ["loren"]
summary:
    initialVersion: "1.23.10"
---

Returns a table that is shared by all mods.

# Syntax
```lua
GetShared()
```

# Examples
Store something in the table in one mod:
```lua
local SharedTable = GetShared()

SharedTable.Example = "Potato"
```

And then print it from another mod afterwards:
```lua
local SharedTable = GetShared()

print(SharedTable.Example) -- prints "Potato"
```

# Notes
No additional notes.

# Version History
## 1.23.10
Added this function.