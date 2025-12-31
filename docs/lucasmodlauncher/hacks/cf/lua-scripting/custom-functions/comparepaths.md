---
title: ComparePaths
description: "Compares two paths with options to ignore different casing and different slashes."
---

Compares two paths with options to ignore different casing and different slashes.

# Syntax

```lua
ComparePaths( <path1>, <path2>, [<case_insensitive>, <slash_insensitive>] )
```

* **path1**: The first path.
* **path2**: The second path.
* **case_insensitive**: Whether or not the comparison is case insensitive. 
    * Optional, defaults to true.
* **slash_insensitive**: Whether or not the comparison is slash insensitive. 
    * Optional, defaults to true.

# Examples
```lua
-- Result is true
local Result = ComparePaths("art\\cars\\famil_v.p3d", "art/cars/famil_v.p3d")

-- Result is false, the capitalization is different.
local Result = ComparePaths("ART\\CARS\\FAMIL_V.p3d", "art/cars/famil_v.p3d", false)

-- Result is false, the slashes are different.
local Result = ComparePaths("ART\\CARS\\FAMIL_V.p3d", "ART/CARS/FAMIL_V.p3d", true, false)
```

# Notes
No additional notes.

# Version History
## 1.19
Fixed an issue where this function was always case sensitive and always slash sensitive.

## Unknown Version
Added this function.