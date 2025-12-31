---
title: AddVehicleCharacterSuppressionCharacter
description: "Set the character whose suppression status will cause this character to not be in the vehicle."
summary:
    initialVersion: "1.19"
---

Set the character whose suppression status (set via [SuppressDriver](/hitandrun/scripting/mfk-commands/suppressdriver.md) in the Level's load script) will cause this character to not be in the vehicle.

# Syntax
{{ tabs }}
{{ tab CON }}
```js
AddVehicleCharacterSuppressionCharacter( character, suppression_character );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddVehicleCharacterSuppressionCharacter( character, suppression_character )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character who will get suppressed.
* **suppression_character**: The name of the character whose suppression will after this character.
    * By default, the character themselves will already be a suppression character.
    * **none**: Use "none" to prevent this character from getting suppressed altogether.

# Examples
{{ tabs }}
{{ tab CON }}
```js
AddVehicleCharacter("askinner");

// Maybe add a real Agnes NPC to Skinner's car and suppress her when Skinner is suppressed, like normal.
AddVehicleCharacterSuppressionCharacter("askinner", "skinner");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddVehicleCharacter("askinner")

-- Maybe add a real Agnes NPC to Skinner's car and suppress her when Skinner is suppressed, like normal.
Game.AddVehicleCharacterSuppressionCharacter("askinner", "skinner")
```
{{ endtab }}
{{ endtabs }}
​

# Notes
This can only be used on characters added with [AddVehicleCharacter](addvehiclecharacter.md).

# History
## 1.19
Added this command.