---
title: completedwasps
description: "This type of objective requires the player to destroy a certain amount of Wasp Cameras in the level to pass the stage."
summary:
    initialVersion: "1.18"
---

This type of objective requires the player to destroy a certain amount of Wasp Cameras in the level to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("completedwasps");
	// Optional: Set the amount of wasps the player must have destroyed. Defaults to 1.
	SetObjTotal(3);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("completedwasps")
	-- Optional: Set the amount of wasps the player must have destroyed. Defaults to 1.
	Game.SetObjTotal(3)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this objective type.