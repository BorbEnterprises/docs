---
title: "follow"
description: "This type of objective requires an AI vehicle to reach a specific locator (specified as a series of waypoints) to pass the stage."
authors: [ 2, 2116 ]
---

This type of objective requires an AI vehicle to reach a specific locator (specified as a series of waypoints) to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Specify the name of a Type 0 Event Locator the vehicle will drive to. 
// At least 1 waypoint is required for the stage to function.
AddStageWaypoint("m5_van_path6");

AddObjective("follow");
	// Required: Specify the vehicle that the player must follow.
	SetObjTargetVehicle("cVan");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Specify the name of a Type 0 Event Locator the vehicle will drive to. 
-- At least 1 waypoint is required for the stage to function.
Game.AddStageWaypoint("m5_van_path6")

Game.AddObjective("follow")
	-- Required: Specify the vehicle that the player must follow.
	Game.SetObjTargetVehicle("cVan")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
These objectives are typically used in conjunction with a [[../MissionConditions/followdistance.md]] condition in order to require the player to maintain a certain distance between themselves and the vehicle.