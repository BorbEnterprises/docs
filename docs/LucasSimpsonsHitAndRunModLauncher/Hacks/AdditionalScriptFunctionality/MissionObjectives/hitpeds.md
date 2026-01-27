---
title: "hitpeds"
description: "This type of objective requires the player to kick pedestrians to pass the stage."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
---

This type of objective requires the player to kick pedestrians to pass the stage.

# Examples
## Basic Example
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("hitpeds");
	// Optional: Specify specific character models that the player has to kick. Defaults to all characters.
	AddObjTargetModel("marge");
	AddObjTargetModel("bart");

	// Optional: Specify the amount of times they have to kick them. Defaults to 1.
	SetObjTotal(3);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("hitpeds")
	-- Optional: Specify specific character models that the player has to kick. Defaults to all characters.
	Game.AddObjTargetModel("marge")
	Game.AddObjTargetModel("bart")

	-- Optional: Specify the amount of times they have to kick them. Defaults to 1.
	Game.SetObjTotal(3)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

## Exploding NPCs Example
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddObjective("hitpeds");
		SetObjTotal(8);
		SetObjExplosion(24, 0.25, 3);
		SetObjSound("generic_car_explode");

		AddObjTargetModel("boy1");
		AddObjTargetModel("boy2");
		AddObjTargetModel("boy3");
		AddObjTargetModel("boy4");
		AddObjTargetModel("girl1");
		AddObjTargetModel("girl2");
		AddObjTargetModel("girl3");
		AddObjTargetModel("girl4");
		AddObjTargetModel("rednk1");
		AddObjTargetModel("bart");
		AddObjTargetModel("lisa");
		AddObjTargetModel("ralph");
		AddObjTargetModel("milhouse");
		AddObjTargetModel("nelson");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.AddObjective("hitpeds")
		Game.SetObjTotal(8)
		Game.SetObjExplosion(24, 0.25, 3)
		Game.SetObjSound("generic_car_explode")

		Game.AddObjTargetModel("boy1")
		Game.AddObjTargetModel("boy2")
		Game.AddObjTargetModel("boy3")
		Game.AddObjTargetModel("boy4")
		Game.AddObjTargetModel("girl1")
		Game.AddObjTargetModel("girl2")
		Game.AddObjTargetModel("girl3")
		Game.AddObjTargetModel("girl4")
		Game.AddObjTargetModel("rednk1")
		Game.AddObjTargetModel("bart")
		Game.AddObjTargetModel("lisa")
		Game.AddObjTargetModel("ralph")
		Game.AddObjTargetModel("milhouse")
		Game.AddObjTargetModel("nelson")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}