---
title: collectcoins
description: "This type of objective requires the player collect coins to pass the stage."
summary:
    initialVersion: "1.18"
---

This type of objective requires the player collect coins to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("collectcoins");
	// Optional: Set the amount of coins the player has to collect. Defaults to 1.
	SetObjTotal(12);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("collectcoins")
	-- Optional: Set the amount of coins the player has to collect. Defaults to 1.
	Game.SetObjTotal(12)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this objective type.