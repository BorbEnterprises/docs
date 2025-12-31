---
title: FixSlashes
description: "Returns a version of the given path with modified slashes."
---

Returns a version of the given path with modified slashes.

# Syntax
```lua
FixSlashes( <path>, [<to_windows>, <from_windows>])
```

* **path**: The path to modify.
* **to_windows**: Convert the path to have back slashes (`\`).
* **from_windows**: Convert the path to have forward slashes (`/`).

# Examples
```lua
--- Returns "scripts/missions/level01/level.mfk"
local Path1 = FixSlashes("scripts\\missions\\level01\\level.mfk", false, true)

--- Returns "scripts\missions\level01\level.mfk"
local Path2 = FixSlashes("scripts/missions/level01/level.mfk", true, false)
```

# Notes
Only one of the 2nd and 3rd arguments should be set to true.

# Version History
## Unknown Version
Added this function.