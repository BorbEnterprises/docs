---
title: reachspeed
description: "This type of objective requires the player to reach a certain speed to pass the stage."
summary:
    initialVersion: "1.18"
---

This type of objective requires the player to reach a certain speed to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("reachspeed");
	// Required: Set the speed that the player has to reach to pass.
	SetObjSpeedKMH(120);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("reachspeed")
	-- Required: Set the speed that the player has to reach to pass.
	Game.SetObjSpeedKMH(120)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this objective type.
