---
title: ReadFile
description: "Read the file at the given path."
---

Read the file at the given path.

# Syntax
```lua
ReadFile( <path> )
```

* **path**: The path of the file to read.

# Examples
```lua
local RewardsScript = ReadFile("/GameData/scripts/missions/rewards.mfk")
```

# Notes
No additional notes.

# Version History
## 1.24
Fixed a memory leak when Lua failed to allocate memory to return the result of a call to the `ReadFile` function.

## Unknown Version
Added this function.