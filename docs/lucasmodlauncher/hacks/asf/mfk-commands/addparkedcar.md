---
title: AddParkedCar
description: "Adds a car to the parked cars list for the level. This can be used to add a parked car without also adding it to a traffic group."
summary:
    initialVersion: "1.22"
---

Adds a car to the parked cars list for the level. This can be used to add a parked car without also adding it to a traffic group using [AddTrafficModel](/hitandrun/scripting/mfk-commands/addtrafficmodel.md).

# Context
{{ snippet hitandrun/command-contexts/level-init }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddParkedCar( car_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddParkedCar( car_name )
```
{{ endtab }}
{{ endtabs }}

* **car_name**: The name of the car to add to the parked cars list.


# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddParkedCar("famil_v");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddParkedCar("famil_v")
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# History
## 1.22
Added this command.