---
title: RemoveStageVehicleCharacter
description: "Remove a character from a stage vehicle or the player's car upon reaching the stage."
summary:
    initialVersion: "1.19"
---

Remove a character from a stage vehicle or the player's car upon reaching the stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

Additionally, this should only be called on characters previously added to the car with [AddStageVehicleCharacter](addstagevehiclecharacter.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
RemoveStageVehicleCharacter( car, character );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.RemoveStageVehicleCharacter( car, character )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car to remove the character from.
    * **current**: In this case, current refers to the car the player had when the character was added. Not the one they have in the stage this is called.
* **character**: The name of the character to remove from the car.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// Add Apu here.
	AddStageVehicleCharacter("current","apu");

	AddObjective("dummy");
		...
	CloseObjective();
CloseStage();

AddStage();
	// Remove him here.
	RemoveStageVehicleCharacter("current","apu");

	AddObjective("dummy");
		...
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua    
Game.AddStage()
	-- Add Apu here.
	Game.AddStageVehicleCharacter("current","apu")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()

Game.AddStage()
	-- Remove him here.
	Game.RemoveStageVehicleCharacter("current","apu")

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