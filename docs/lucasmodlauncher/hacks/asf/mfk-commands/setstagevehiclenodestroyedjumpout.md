---
title: SetStageVehicleNoDestroyedJumpOut
description: "Sets whether or not the driver of the vehicle will jump out when it's destroyed."
summary:
    initialVersion: "1.18.1"
---

Sets whether or not the driver of the vehicle will jump out when it's destroyed.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleNoDestroyedJumpOut( vehicle_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleNoDestroyedJumpOut( vehicle_name )
```
{{ endtab }}
{{ endtabs }}

* **vehicle_name**: The name of the vehicle to apply this behaviour to.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddStageVehicle("skinn_v","m1_skinn_v","NULL","Missions\level01\M1race.con", "skinner");

	// Skinner will go down with his car...
	SetStageVehicleNoDestroyedJumpOut("skinn_v");

	AddObjective("dummy");
	CloseObjective();
CloseStage();

```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 	
	Game.AddStageVehicle("skinn_v","m1_skinn_v","NULL","Missions\\level01\\M1race.con", "skinner")

	-- Skinner will go down with his car...
	Game.SetStageVehicleNoDestroyedJumpOut("skinn_v")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
This command is not intended for use on the player's car. Doing so will cause it to apply to the car until it is deleted (even if the mission has already ended).

There are currently complications with using this on a vehicle whose driver was added with Radical's [AddDriver](/hitandrun/scripting/mfk-commands/adddriver.md) command.

# Version History
## 1.18.1
Added this command.