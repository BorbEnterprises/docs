---
title: GetModTitle
description: "Returns the title of the specified mod or the current mod if none is specified."
---

Returns the title of the specified mod or the current mod if none is specified.

This returns `nil` if called with the name of a mod that is not enabled.

# Syntax
```lua
GetModTitle( [<mod_name>] )
```

* **mod_name**: The name of the mod whose title you'd like to get.

# Examples
```lua
local CurrentModTitle = GetModTitle()

print(CurrentModTitle .. " loaded!")
```

# Notes
No additional notes.

## Version History
## 1.22
Added this function.