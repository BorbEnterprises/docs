---
title: Exists
description: "Returns whether or not the specified path exists."
---

Returns whether or not the specified path exists.

# Syntax
```lua
Exists ( <path>, <is_file>, <is_directory> )
```

* **path**: The path to check.
* **is_file**: Return true if the path is a file. 
* **is_directory**: Return true if the path is a directory.

# Examples
```lua
if Exists(GetModPath() .. "/Resources/test.lua", true, false) then
    -- do stuff if that file exists
end
```

# Notes
No additional notes.

# Version History
## Unknown Version
Added this function.