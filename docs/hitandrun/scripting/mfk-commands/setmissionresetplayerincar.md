---
title: SetMissionResetPlayerInCar
description: "Forces the player into their vehicle and sets the position the vehicle is placed upon restarting a mission."
authors: ["colou"]
---

Forces the player into their vehicle and sets the position the vehicle is placed upon restarting a mission.

# Context
{{ snippet hitandrun/command-contexts/mission-init-root }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetMissionResetPlayerInCar( vehicle_locator );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetMissionResetPlayerInCar( vehicle_locator )
```
{{ endtab }}
{{ endtabs }}

* **vehicle_locator**: The name of the [Type 3 Locator](/pure3d/chunk-types/chunk-3000005.md#this_types_type3) where the player's vehicle is placed.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	...
	
	SetMissionResetPlayerInCar("m1_carstart");

	AddStage();		
		...		
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")
	...
	
	Game.SetMissionResetPlayerInCar("m1_carstart")

	Game.AddStage()	
		...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
When both this command and [SetMissionResetPlayerOutCar](/hitandrun/scripting/mfk-commands/setmissionresetplayeroutcar.md) are used, the player will be placed at the **player_locator** from **SetMissionResetPlayerOutCar**, and the vehicle will be placed at whichever **vehicle_locator** is specified last in the script.
