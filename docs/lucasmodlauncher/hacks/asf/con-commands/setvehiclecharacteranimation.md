---
title: SetVehicleCharacterAnimation
description: "Set the animation that the character will use in the car."
summary:
    initialVersion: "1.19"
---

Set the animation that the character will use in the car.

# Syntax
{{ tabs }}
{{ tab CON }}
```js
SetVehicleCharacterAnimation( character, animation, [bobbing] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetVehicleCharacterAnimation( character, animation, [bobbing] )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character.
* **animation**: The name of the animation.
    * This animation must be specified in the NPD animation set.
* **bobbing**: Whether or not the character will bob up and down.
    * This defaults to false if this function is called.
    * This will also make the character lean side-to-side when appropriate.
    * Though this is dependent on the user's Bug Fixes setting for this.

# Examples
{{ tabs }}
{{ tab CON }}
```js
AddVehicleCharacter("apu");
SetVehicleCharacterAnimation("apu","surf_cycle");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddVehicleCharacter("apu")
Game.SetVehicleCharacterAnimation("apu","surf_cycle")
```
{{ endtab }}
{{ endtabs }}

# Notes
This can only be used on characters added with [AddVehicleCharacter](addvehiclecharacter.md).

# History
## 1.19
Added this command.