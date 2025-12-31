---
title: ReadFileOffset
description: "Read part of a file at the given path."
summary:
    initialVersion: "1.24"
---

Read part of a file at the given path.

# Syntax
```lua
ReadFileOffset( <path>, <offset>, <length> )
```

* **path**: The path of the file to read.
* **offset**: The offset in the file in bytes. This value is 1 based.
* **length**: The amount of bytes to read.

# Examples
```lua
-- Random example to read a small, probably useless, part of L1_TERRA
local FilePart = ReadFileOffset("/GameData/art/L1_TERRA.p3d", 657, 512)
```

# Notes
Reading past the end of the file will return a shorter amount than what you requested.

# Version History
## 1.24
Added this function.