---
title: AddStageVehicle
description: "Adds a loaded vehicle to the world in a mission."
authors: ["loren"]
---

This command adds a loaded vehicle to the world in a mission.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddStageVehicle( car, locator, behaviour, [con_file, driver] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStageVehicle( car, locator, behaviour, [con_file, driver] )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car to add.
* **locator**: The name of the [Locator Type 3](/pure3d/chunk-types/chunk-3000005.md#type-3-car-start-locator) to place the car on.
* **behaviour**: The type of [Vehicle Behaviour](/hitandrun/misc/vehicle-behaviours.md) to give the car.
* **con_file**: The CON file to use on the car.
    * Optional, defaults to the car's CON file in the `scripts\cars` folder if omitted.
* **driver**: The driver of the vehicle. This only works if the `con_file` does not call [SetDriver](/hitandrun/scripting/con-commands/setdriver.md).
    * Optional, defaults to no driver if omitted (unless the specified `con_file` sets a driver).

# Examples
{{ tabs }}
{{ tab MFK }}
This example adds Skinner's car and activates it immediately with [Chase AI](/hitandrun/misc/vehicle-behaviours.md#chase).
```js
SelectMission("m1");
	...

	AddStage();
		// Add Skinner with chase AI right away.
		AddStageVehicle("skinn_v","m1_skinner_car","chase","missions\\l1m0\\skinner.con","skinner");

		AddObjective("dummy");
		
		CloseObjective();
	CloseStage();
CloseMission();
```

This example adds Skinner's car with no AI and then activates it in the following stage with [ActivateVehicle](activatevehicle.md).
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
This example adds Skinner's car and activates it immediately with [Chase AI](/hitandrun/misc/vehicle-behaviours.md#chase).
```lua
Game.SelectMission("m1")
	...

	Game.AddStage()
		-- Add Skinner with chase AI right away.
		Game.AddStageVehicle("skinn_v","m1_skinner_car","chase","missions\\l1m0\\skinner.con","skinner")

		Game.AddObjective("dummy")
		
		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```

This example adds Skinner's car with no AI and then activates it in the following stage with [ActivateVehicle](activatevehicle.md).
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