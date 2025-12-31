---
title: GetSetting
description: "Returns the value of a setting in a mod."
---

Returns the value of a setting in a mod.

# Syntax
```lua
GetSetting( <setting_name>, [<mod_name>] )
```

* **setting_name**: The name of the setting to get the value of.
* **mod_name**: The mod you want to get the setting from from. Optional, defaults to the mod that called the function.

# Examples
```lua
-- Get the difficulty setting of the current mod.
local Difficulty = GetSetting("Difficulty")

-- Check some other setting in another mod.
local SomeOtherSetting = GetSetting("SomeOtherSetting","AnotherMod")
```

# Notes
No additional notes.

# Version History
## 1.23.10

* Fixed an issue where this function read the low 32-bits of the 64-bit signed integer setting values as unsigned and casted that to a 64-bit signed integer to give it to Lua. This caused negative integer setting values to wrap as if they were 32-bit unsigned values.
	* If you'd like, you can use something like `if SettingValue > 2147483647 then SettingValue = SettingValue - 4294967296 end` to support old versions of the Mod Launcher.

## Unknown Version
Added this function.