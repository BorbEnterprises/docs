---
title: getin
description: "This type of objective requires the player to enter a car to pass the stage."
authors: ["borb"]
---

This type of objective requires the player to enter a car to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
This example demonstrates the general usage of the objective, simply requiring the player to enter any vehicle to pass the stage.
```js
// The player must enter a car to pass the objective.
AddObjective("getin");
	// Despite Radical's use of SetObjTargetVehicle(), it has no effect in this objective.
	SetObjTargetVehicle("current");
CloseObjective();
```

This example demonstrates this objective being used in a forced car mission. The player will be required to enter the forced car specifically rather than a traffic vehicle or parked car.

```js
SelectMission("m3");
InitLevelPlayerVehicle("forcedcar_v", "m3_forced_carstart", "OTHER");
	...
	AddStage();
		// The player must enter the specified car, provided it exists when the MFK file is executed.
		AddObjective("getin", "forcedcar_v");
			// Despite Radical's use of SetObjTargetVehicle(), it has no effect in this objective.
			SetObjTargetVehicle("current");
		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
This example demonstrates the general usage of the objective, simply requiring the player to enter any vehicle to pass the stage.
```lua
-- The player must enter a car to pass the objective.
Game.AddObjective("getin")
	-- Despite Radical's use of SetObjTargetVehicle(), it has no effect in this objective.
	Game.SetObjTargetVehicle("current")
Game.CloseObjective()
```

This example demonstrates this objective being used in a forced car mission. The player will be required to enter the forced car specifically rather than a traffic vehicle or parked car.

```lua
Game.SelectMission("m3")
Game.InitLevelPlayerVehicle("forcedcar_v", "m3_forced_carstart", "OTHER")
	...
	Game.AddStage()
		-- The player must enter the specified car, provided it exists when the MFK file is executed.
		Game.AddObjective("getin", "forcedcar_v")
			-- Despite Radical's use of SetObjTargetVehicle(), it has no effect in this objective.
			Game.SetObjTargetVehicle("current")
		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
* If using a car as the second argument to AddObjective() as outlined in the forced car example, the car must exist when the MFK script is loaded. If the vehicle does not exist at this time, this argument will be ignored.
* If using a car as the second argument to AddObjective() as outlined in the forced car example, "getin" and the car's name must be the only two arguments, no arrow flags can be specified.
