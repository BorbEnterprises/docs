---
title: GetSettings
description: "Returns the values of all of the settings of the a mod as a table."
---

Returns the values of all of the settings of the a mod as a table.

# Syntax
```lua
GetSettings( [<mod_name>] )
```

* **mod_name**: The mod you want to get setting values from. 
    * Optional, defaults to the mod that called the function.

# Examples
```lua
-- Get settings of the current mod
local Settings = GetSettings()

-- Get settings of another mod
local Settings = GetSettings("AnotherMod")
```

# Notes
When returning the value of MultipleChoice type settings this function returns them 1 based instead of 0 based like the older [GetSetting](getsetting.md) function.

```lua
-- To demonstrate, here's an example.
-- For this example, let's assume that the Difficulty setting is on the first Option.

-- Difficulty would be 0
local Difficulty = GetSetting("Difficulty")
​
-- Settings.Difficulty would be 1
local Settings = GetSettings()
```

# History
## 1.23.10

* Fixed an issue where this function read the low 32-bits of the 64-bit signed integer setting values as unsigned and casted that to a 64-bit signed integer to give it to Lua. This caused negative integer setting values to wrap as if they were 32-bit unsigned values.
	* If you'd like, you can use something like `if SettingValue > 2147483647 then SettingValue = SettingValue - 4294967296 end` to support old versions of the Mod Launcher.

## 1.19
Added this command.