---
title: SetVehicleCharacterScale
description: "Set the scale of the character."
summary:
    initialVersion: "1.19"
---

Set the scale of the character.

# Syntax
{{ tabs }}
{{ tab CON }}
```js
SetVehicleCharacterScale( character, [scale] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetVehicleCharacterScale( character, [scale] )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character.
* **scale**: The scale of the character.
    * The default value is the scale defined in the CON file for said car.

# Examples
{{ tabs }}
{{ tab CON }}
```js
AddVehicleCharacter("apu");
SetVehicleCharacterScale("apu", 2);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddVehicleCharacter("apu")
Game.SetVehicleCharacterScale("apu", 2)
```
{{ endtab }}
{{ endtabs }}

# Notes
This can only be used on characters added with [AddVehicleCharacter](addvehiclecharacter.md).

# History
## 1.19
Added this command.