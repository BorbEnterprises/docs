---
title: GetPathParent
description: "Returns the parent path of the specified file path."
---

Returns the parent path of the specified file path.

This will return the file name if it is only given a file name.

# Syntax
```lua
GetPathParent( <path>, [<windows>] )
```

* **path**: The file path that you want to get the parent path out of.
* **windows**: TODO <!-- Ask Lucas again -->
    * Optional.

# Examples
```lua
-- Returns "scripts\missions\level01"
GetPathParent("scripts\\missions\\level01\\level.mfk")

-- Returns "level.mfk"
GetPathParent("level.mfk")
```

# Notes
No additional notes.

# Version History
## Unknown Version
Added this function.