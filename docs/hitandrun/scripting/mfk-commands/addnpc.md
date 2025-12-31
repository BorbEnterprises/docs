---
title: AddNPC
description: Adds an NPC to the world at the specified Type 3 Locator.
authors: ["borb","loren"]
---

Adds an NPC to the world at the specified [Type 3 Locator](/pure3d/chunk-types/chunk-3000005.md#this_types_type3).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddNPC( npc, locator, [interior] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddNPC( npc, locator, [interior] )
```
{{ endtab }}
{{ endtabs }}

* **npc**: The name of the NPC to add.
* **locator**: The name of the [Type 3 Locator](/pure3d/chunk-types/chunk-3000005.md#this_types_type3) to place the NPC on.
* **interior**: The name of the interior the NPC is located inside.
	* Optional.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m2sd");
    ...
    
    AddStage();
        AddObjective("dummy");
            AddNPC("ned", "m2_ned_sd");
        CloseObjective();
    CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m2sd")
    ...
    
    Game.AddStage()
        Game.AddObjective("dummy")
            Game.AddNPC("ned", "m2_ned_sd")
        Game.CloseObjective()
    Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.