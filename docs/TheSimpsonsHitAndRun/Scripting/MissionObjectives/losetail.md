---
title: "losetail"
description: "This type of objective requires the player to escape an AI car that is pursuing them."
authors: [ 2116 ]
---

This type of objective requires the player to escape an AI car that is pursuing them.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("losetail");
	// Required: Specify the vehicle that the player needs to escape.
	SetObjTargetVehicle("skinn_v");

	// Required: Specify the distance that the player needs to get away from the target vehicle.
	SetObjDistance(150);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("losetail")
	-- Required: Specify the vehicle that the player needs to escape.
	Game.SetObjTargetVehicle("skinn_v")

	-- Required: Specify the distance that the player needs to get away from the target vehicle.
	Game.SetObjDistance(150)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}