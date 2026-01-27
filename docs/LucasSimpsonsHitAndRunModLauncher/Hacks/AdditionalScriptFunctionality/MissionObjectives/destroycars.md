---
title: "destroycars"
description: "This type of objective requires the player to destroy one or more cars to pass the stage."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
---

This type of objective requires the player to destroy one or more cars to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("destroycars");
	// Optional: Specify specific car models the player must destroy. Defaults to all cars.
	AddObjTargetModel("minivanA");
	AddObjTargetModel("glastruc");

	// Optional: Specify the amount of cars the player must destroy. Defaults to 1.
	SetObjTotal(3);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("destroycars")
	-- Optional: Specify specific car models the player must destroy. Defaults to all cars.
	Game.AddObjTargetModel("minivanA")
	Game.AddObjTargetModel("glastruc")

	-- Optional: Specify the amount of cars the player must destroy. Defaults to 1.
	Game.SetObjTotal(3)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}