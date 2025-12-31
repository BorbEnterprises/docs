---
title: SetMissionResetPlayerOutCar
description: "Sets the positions where the player and their vehicle are placed upon restarting a mission."
authors: ["colou"]
---

Sets the positions where the player and their vehicle are placed upon restarting a mission.

# Context
{{ snippet hitandrun/command-contexts/mission-init-root }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetMissionResetPlayerOutCar( player_locator, vehicle_locator );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetMissionResetPlayerOutCar( player_locator, vehicle_locator )
```
{{ endtab }}
{{ endtabs }}

* **player_locator**: The name of the [Type 3 Locator](/pure3d/chunk-types/chunk-3000005.md#this_types_type3) where the player is placed.
* **vehicle_locator**: The name of the [Type 3 Locator](/pure3d/chunk-types/chunk-3000005.md#this_types_type3) where the player's vehicle is placed.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	...

	SetMissionResetPlayerOutCar("m4_homer_start", "m4_carstart");

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

	Game.SetMissionResetPlayerOutCar("m4_homer_start", "m4_carstart")

	Game.AddStage()
		...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
When both this command and [SetMissionResetPlayerInCar](/hitandrun/scripting/mfk-commands/setmissionresetplayerincar.md) are used, the player will be placed at the **player_locator** from **SetMissionResetPlayerOutCar**, and the vehicle will be placed at whichever **vehicle_locator** is specified last in the script.
