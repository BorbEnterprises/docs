---
title: SetStageVehicleAllowSeatSlide
description: "Sets whether or not the stage vehicle allows seat slide."
summary:
    initialVersion: "1.19"
---

Sets whether or not the stage vehicle allows seat slide.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleAllowSeatSlide( car, allow_seat_slide );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleAllowSeatSlide( car, allow_seat_slide )
```
{{ endtab }}
{{ endtabs }}

car: The name of the car.
current: The player's current vehicle.
allow_seat_slide: Whether or not to allow seat slide.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddStageVehicleCharacter("current", "lisa");

	// Lisa is now in the passenger seat so we need to block it.
	SetStageVehicleAllowSeatSlide("current", 0);

	AddObjective("dummy");
	CloseObjective();
CloseStage();

AddStage();
	RemoveStageVehicleCharacter("current", "lisa");

	// Lisa is no longer in the seat so re-enable seat slide
	SetStageVehicleAllowSeatSlide("current", 1);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	Game.AddStageVehicleCharacter("current", "lisa")

	-- Lisa is now in the passenger seat so we need to block it.
	Game.SetStageVehicleAllowSeatSlide("current", 0)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()

Game.AddStage() 
	Game.RemoveStageVehicleCharacter("current", "lisa")

	-- Lisa is no longer in the seat so re-enable seat slide
	Game.SetStageVehicleAllowSeatSlide("current", 1)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
This command is really only useful for the player's car at this time as there is no intended way to enter a stage vehicle.

# Version History
## 1.19
Added this command.