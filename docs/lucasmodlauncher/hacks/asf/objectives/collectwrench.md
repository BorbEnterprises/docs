---
title: collectwrench
description: "This type of objective requires the player to collect a wrench to pass the stage."
summary:
    initialVersion: "1.18"
---

This type of objective requires the player to collect a wrench to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("collectwrench");
	// Optional: Set the amount of wrenches the player has to collect. Defaults to 1.
	SetObjTotal(1);
CloseObjective();  
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("collectwrench")
	-- Optional: Set the amount of wrenches the player has to collect. Defaults to 1.
	Game.SetObjTotal(1)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this objective type.