---
title: SetVehicleCharacterJumpOut
description: "Set the character to jump out of the vehicle is destroyed."
summary:
    initialVersion: "1.19"
---

Set the character to jump out of the vehicle is destroyed.

# Syntax
{{ tabs }}
{{ tab CON }}
```js
SetVehicleCharacterJumpOut( character, [direction] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetVehicleCharacterJumpOut( character, [direction] )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character.
* **direction**: The direction in which they will jump. This is an angle from 0 to 360 degrees.
    * The default value of this depends on the character's position relative to the origin of the car.

# Examples
{{ tabs }}
{{ tab CON }}
```js
AddVehicleCharacter("apu");
SetVehicleCharacterJumpOut("apu", 180);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddVehicleCharacter("apu")
Game.SetVehicleCharacterJumpOut("apu", 180)
```
{{ endtab }}
{{ endtabs }}

# Notes
This can only be used on characters added with [AddVehicleCharacter](addvehiclecharacter.md).

# History
## 1.19
Added this command.