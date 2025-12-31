---
title: SetStageVehicleCharacterJumpOut
description: "Set the character to jump out of the vehicle when it's destroyed."
summary:
    initialVersion: "1.19"
---

Set the character to jump out of the vehicle when it's destroyed.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

Additionally, this should only be called in the same stage the vehicle character was added with [AddStageVehicleCharacter](addstagevehiclecharacter.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleCharacterJumpOut( car, character, [direction] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleCharacterJumpOut( car, character, [direction] )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car.
	* **current**: The player's current car.
* **character**: The name of the character.
* **direction**: The direction that the character will jump out of the vehicle. This is an angle from 0 to 360 degrees.
	* The default value of this depends on the character's position relative to the origin of the car.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();    
	AddStageVehicle("cVan","m1_cVan","NULL");

	AddStageVehicleCharacter("cVan", "lisa");
	SetStageVehicleCharacterJumpOut("cVan", "lisa", 270);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	Game.AddStageVehicle("cVan","m1_cVan","NULL")

	Game.AddStageVehicleCharacter("cVan", "lisa")
	Game.SetStageVehicleCharacterJumpOut("cVan", "lisa", 270)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.19
Added this command.