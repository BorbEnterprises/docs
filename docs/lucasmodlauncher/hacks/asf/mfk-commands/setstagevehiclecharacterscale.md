---
title: SetStageVehicleCharacterScale
description: "Set the scale of the character in the stage vehicle."
summary:
    initialVersion: "1.19"
---

Set the scale of the character in the stage vehicle.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

Additionally, this should only be called on characters previously added to the car with [AddStageVehicleCharacter](addstagevehiclecharacter.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleCharacterScale( car, character, scale );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleCharacterScale( car, character, scale )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car the character is in.
* **character**: The name of the character.
* **scale**: Set the scale of the character. 
    * Defaults to the car's character scale set with [SetCharacterScale](/hitandrun/scripting/con-commands/setcharacterscale.md).

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();    
	AddStageVehicle("cVan","m1_cVan","NULL","cVan.con");
	AddStageVehicleCharacter("cVan", "bart", "sl", 0);	

	// Big Bort
	SetStageVehicleCharacterScale("cVan","bart", 3);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	Game.AddStageVehicle("cVan","m1_cVan","NULL","cVan.con")
	Game.AddStageVehicleCharacter("cVan", "bart", "sl", 0)

	-- Big Bort
	Game.SetStageVehicleCharacterScale("cVan","bart", 3)

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