---
title: SetVehicleCharacterVisible
description: "Set whether or not the character is visible."
summary:
    initialVersion: "1.19"
---

Set whether or not the character is visible.

This can be used to force a character to be visible in a car where the driver and player character are not.

# Syntax
{{ tabs }}
{{ tab CON }}
```js
SetVehicleCharacterVisible( character );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetVehicleCharacterVisible( character )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character.

# Examples
{{ tabs }}
{{ tab CON }}
```js
AddVehicleCharacter("apu");
SetVehicleCharacterVisible("apu");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddVehicleCharacter("apu")
Game.SetVehicleCharacterVisible("apu")
```
{{ endtab }}
{{ endtabs }}

# Notes
This can only be used on characters added with [AddVehicleCharacter](addvehiclecharacter.md).

# History
## 1.19
Added this command.