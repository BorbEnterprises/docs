---
title: "collectwrench"
description: "This type of objective requires the player to collect a wrench to pass the stage."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
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