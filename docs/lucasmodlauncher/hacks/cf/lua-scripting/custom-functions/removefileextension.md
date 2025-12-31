---
title: RemoveFileExtension
description: "Returns the the specified filename path.Returns the given file path or file name without the file extension."
---

Returns the the specified filename path.Returns the given file path or file name without the file extension.

# Syntax
```lua
RemoveFileExtension( <path> )
```

* **path**: The path or filename of the file you want to remove the extension from.

# Examples
```lua
-- Returns "example"
RemoveFileExtension("example.mfk")

-- Returns "scripts\example"
RemoveFileExtension("scripts\\example.mfk")
```

# Notes
No additional notes.

# Version History
## Unknown Version
Added this function.