---
title: GetLauncherVersion
description: "Returns the current version of the Mod Launcher."
authors: ["loren","lucasc190","proddy"]
---

Returns the current version of the Mod Launcher as a string.

# Syntax
```lua
GetLauncherVersion()
```

# Examples
```lua
-- Separates a version string into a table of numbers.
function GetVersionParts(Version)
	local tbl = {}
	
    for part in Version:gmatch("[^%.]+") do
       tbl[#tbl + 1] = tonumber(part)
	end
	
    return tbl
end

-- Compares version table. Returns positive is Version1 is newer, negative is Version1 is older or 0 if equal.
function CompareVersion(Version1, Version2)
	local Part1, Part2
	
    for i = 1, math.max(#Version1, #Version2) do
        Part1 = Version1[i] or 0
        Part2 = Version2[i] or 0
        
        if Part1 < Part2 then return -1 end
        if Part1 > Part2 then return 1 end
	end
	
    return 0
end

local LauncherVersion = GetLauncherVersion()

-- IsOldVersion will be true if launcher version is before 1.23.9
IsOldVersion = CompareVersion(GetVersionParts(LauncherVersion), {1, 23, 9}) < 0
```

# Notes
No additional notes.

# Version History
## 1.19
Added this function.
