---
title: SetStageVehicleAbductable
description: "Sets the abductable status of a vehicle."
authors: ["loren"]
summary:
    initialVersion: "1.25"
---

This command sets the abductable status of a vehicle.

This persists until the command is called again, the status is reset with [ResetStageVehicleAbductable](resetstagevehicleabductable.md) or the mission ends.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleAbductable( vehicle, abductable );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleAbductable( vehicle, abductable )
```
{{ endtab }}
{{ endtabs }}

* **vehicle**: The vehicle you would like to reset the abductable flag on.
	* When using `current` for the player's current vehicle, the flag will only affect the car the player has at the time they reach the stage.
* **abductable**: Set whether or not the vehicle will be abductable.
	* The default value of this depends on what is set in [CustomCarSupport](../../custom-car-support.md).

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleAbductable("skinn_v", true);
```
```js
SetStageVehicleAbductable("skinn_v", 1);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleAbductable("skinn_v", true)
```
```lua
Game.SetStageVehicleAbductable("skinn_v", 1)
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.25
Added this command.