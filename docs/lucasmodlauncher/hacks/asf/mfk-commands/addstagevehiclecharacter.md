---
title: AddStageVehicleCharacter
description: "Add a character to a stage vehicle or the player's car for a stage."
summary:
    initialVersion: "1.19"
---

Add a character to a stage vehicle or the player's car for a stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddStageVehicleCharacter( car, character, [joint, rotation] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStageVehicleCharacter( car, character, [joint, rotation] )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car to add the character to.
* **current**: The player's current car.
* **character**: The name of the character to add.
* **joint**: The name of the joint to place the character on. 
    * Defaults to "pl".
    * If the joint does not exist, the character will not be added to the car and any subsequent commands related to them will be ignored.
* **rotation**: The rotation of the character on the joint. 
    * Defaults to 180.
    * 180 is facing forwards in the car since characters are backwards in this game.

# Examples
{{ tabs }}
{{ tab MFK }}
```js    
AddStage();
	// Add Marge to the Passenger Seat of the Player's Car
	AddStageVehicleCharacter("current","marge");

	// Add Lisa and Bart to "cVan"
	//	(you'd probably want to add custom joints to the car for multiple passengers)	
	AddStageVehicle("cVan","m1_cVan","NULL");
	AddStageVehicleCharacter("cVan", "lisa");
	AddStageVehicleCharacter("cVan", "bart", "sl", 0);	// Bart uses the smoke location in this example.

	AddObjective("dummy");

	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua    
Game.AddStage()
	-- Add Marge to the Passenger Seat of the Player's Car
	Game.AddStageVehicleCharacter("current","marge")

	-- Add Lisa and Bart to "cVan"
	--	(you'd probably want to add custom joints to the car for multiple passengers)	
	Game.AddStageVehicle("cVan","m1_cVan","NULL")
	Game.AddStageVehicleCharacter("cVan", "lisa")
	Game.AddStageVehicleCharacter("cVan", "bart", "sl", 0) -- Bart uses the smoke location in this example.

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