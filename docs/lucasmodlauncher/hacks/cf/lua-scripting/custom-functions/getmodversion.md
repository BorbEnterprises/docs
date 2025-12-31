---
title: GetModVersion
description: "Returns the version of the specified mod or the current mod if none is specified."
---

Returns the version of the specified mod or the current mod if none is specified.

# Syntax
```lua
GetModVersion( [<mod_name>] )
```

* **mod_name**: The name of the mod whose version you'd like to get.

# Examples
```lua
local CurrentModVersion = GetModVersion()

print("Version " .. CurrentModVersion .. " loaded!")
```

# Notes
No additional notes.

# Version History
## 1.22
Added this function.