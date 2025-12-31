---
title: jump
description: "This type of objective requires the player to jump to pass the stage."
summary:
    initialVersion: "1.18"
---

This type of objective requires the player to jump to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("jump");
	// Optional: Set the amount of times the player has to jump. Defaults to 1.
	SetObjTotal(3);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("jump")
	-- Optional: Set the amount of times the player has to jump. Defaults to 1.
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