---
title: GetGameLanguage
description: "Returns the current language of the game."
authors: ["loren"]
---

This function returns the current language of the game.

# Syntax
```lua
GetGameLanguage()
```

# Return Values
This function can return the following:

* `"E"`: If the game is in English.
* `"F"`: If the game is in French.
* `"G"`: If the game is in German.
* `"S"`: If the game is in Spanish.

# Examples
```lua
local Language = GetGameLanguage()

if Language == "E" then
	-- Do stuff if the game is English
else
	-- Do other stuff if not
end
```

# Notes
This is affected by the user's game executable as well as by the [Mod Launcher's](/lucasmodlauncher/intro.md) [-language command line argument](/lucasmodlauncher/command-line-arguments.md#hack-hack-support_-language).

# Version History
## 1.25
Added this function.
