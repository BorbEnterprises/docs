---
title: InitLevelPlayerVehicle
description: "This command sets the player's starting vehicle for the mission."
authors: ["legomariofanatic"]
---

{{ snippet hitandrun/command-contexts/mission-init-root }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
InitLevelPlayerVehicle( vehicle_name, locator_name, "OTHER" );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.InitLevelPlayerVehicle( vehicle_name, locator_name, "OTHER" )
```
{{ endtab }}
{{ endtabs }}

* **vehicle_name**: The name of the vehicle to set as the player's initial starting vehicle for the mission.
* **locator_name**: The name of the Type 3 locator to place the vehicle at when starting the mission.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m3");
	...
	\\ This sets Comic Book Guy's vehicle as the starting vehicle for this mission.
	InitLevelPlayerVehicle("comic_v", "m3_cbgcar_sd", "OTHER");
	
	SetForcedCar();
	
	AddStage();
		...
	CloseStage();
	
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m3")
	...
	-- This sets Comic Book Guy's vehicle as the starting vehicle for this mission.
	Game.InitLevelPlayerVehicle("comic_v", "m3_cbgcar_sd", "OTHER")
	
	Game.SetForcedCar()
	
	Game.AddStage()
		...
	Game.CloseStage()

Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
* The vehicle set as the player's starting vehicle will use the same CON file as the version of that vehicle that the player can summon from phone booths.
* This command is often called alongside [SetForcedCar](/hitandrun/scripting/mfk-commands/setforcedcar.md).
