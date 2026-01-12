---
title: "AddPed"
description: "Adds a ped to a ped group."
authors: [ 2 ]
---

This command adds a ped to a ped group.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInitPedGroup.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddPed( character, amount );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddPed( character, amount )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character to add to the ped group.
* **amount**: The maximum amount of this character that will be able to spawn.

# Examples
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Examples/PedGroup.md }}

# Notes
You can add up to 10 unique models to a ped group. Subsequent calls to this command will be ignored.