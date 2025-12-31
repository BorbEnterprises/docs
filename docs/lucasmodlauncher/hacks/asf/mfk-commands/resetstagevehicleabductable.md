---
title: ResetStageVehicleAbductable
description: "Resets the abductable status of a vehicle set with SetStageVehicleAbductable back to the default for the given vehicle."
authors: ["loren"]
summary:
    initialVersion: "1.25"
---

This command resets the abductable status of a vehicle set with [SetStageVehicleAbductable](setstagevehicleabductable.md) back to the default for the given vehicle.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
ResetStageVehicleAbductable( vehicle );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.ResetStageVehicleAbductable( vehicle )
```
{{ endtab }}
{{ endtabs }}

* **vehicle**: The vehicle you would like to reset the abductable flag on.
	* When using `current`, it will reset the flag for the vehicle that was the player's current vehicle when [SetStageVehicleAbductable](setstagevehicleabductable.md) was called.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
ResetStageVehicleAbductable("skinn_v");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.ResetStageVehicleAbductable("skinn_v")
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.25
Added this command.