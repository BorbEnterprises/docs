---
title: ActivateVehicle
description: Activates a vehicle previously added to the world using AddStageVehicle.
authors: ["borb", "loren"]
---

Activates a previously added vehicle.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

Additionally, it must be called with a **car** that has already been added in a previous stage with [AddStageVehicle](addstagevehicle.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
ActivateVehicle( car, locator, behaviour, [driver] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.ActivateVehicle( car, locator, behaviour, [driver] )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car to activate.
* **locator**: The name of the [Type 3 Locator](/pure3d/chunk-types/chunk-3000005.md#this_types_type3) to place the car on when activating it.
    * Radical always uses NULL for this argument, but the behaviour does work.
* **behaviour**: The type of [Vehicle Behaviour](/hitandrun/misc/vehicle-behaviours.md) to give the car.
* **driver**: Set the driver of the vehicle.
	* This argument takes effect immediately, not when reaching the stage.
	* As a result, it's kind of useless and you should just use the 5th argument of [AddStageVehicle](addstagevehicle.md) instead probably.

# Examples

{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	...

	AddStage();
		// Add Skinner with no AI right away.
		AddStageVehicle("skinn_v","m1_skinner_car","NULL","missions\\l1m0\\skinner.con","skinner");

		AddObjective("dummy");
		
		CloseObjective();
	CloseStage();

	AddStage();
		// Then use ActivateVehicle in the next stage to activate him.
		ActivateVehicle("skinn_v","NULL","chase");

		AddObjective("dummy");
		
		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")
	...

	Game.AddStage()
		-- Add Skinner with no AI right away.
		Game.AddStageVehicle("skinn_v","m1_skinner_car","NULL","missions\\l1m0\\skinner.con","skinner")

		Game.AddObjective("dummy")
		
		Game.CloseObjective()
	Game.CloseStage()

	Game.AddStage()
		-- Then use ActivateVehicle in the next stage to activate him.
		Game.ActivateVehicle("skinn_v","NULL","chase")

		Game.AddObjective("dummy")
		
		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.