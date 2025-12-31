---
title: SetStageVehicleCharacterAnimation
description: "Set the animation that a vehicle character will use."
summary:
    initialVersion: "1.19"
---

Set the animation that a vehicle character will use.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

Additionally, this should only be called in the same stage the vehicle character was added with [AddStageVehicleCharacter](addstagevehiclecharacter.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleCharacterAnimation( car, character, animation, [bobbing] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleCharacterAnimation( car, character, animation, [bobbing] )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car the character is on.
    * **current**: The player's current car.
* **character**: The name of character in the car.
* **animation**: The animation to make the character use. 
    * The default animation is "in_car_idle".
* **bobbing**: Whether or not to make the character bob up and down. 
    * Defaults to false (if this function is called).
    * This will also make the character lean side-to-side when appropriate.
        * However, this is dependent whether or not [Steering Animations](../../bug-fixes.md#steering-animations) is enabled in [Bug Fixes](../../bug-fixes.md) by the user.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddStageVehicle("cVan","m1_cVan","NULL","cVan.con");
	
	// Bart uses the smoke location in this example.
	AddStageVehicleCharacter("cVan", "bart", "sl", 0);

	// Make Bart surf on the hood(ish)
	// Note that "surf_cycle" is not in the NPD animation set by default.
	SetStageVehicleCharacterAnimation("cVan","bart","surf_cycle");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	Game.AddStageVehicle("cVan","m1_cVan","NULL")
	
	-- Bart uses the smoke location in this example.
	Game.AddStageVehicleCharacter("cVan", "bart", "sl", 0)

	-- Make Bart surf on the hood(ish)
	-- Note that "surf_cycle" is not in the NPD animation set by default.
	Game.SetStageVehicleCharacterAnimation("cVan","bart","surf_cycle")

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