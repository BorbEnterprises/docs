---
title: AddNPCCharacterBonusMission
description: "Adds an NPC character that hosts a bonus mission to the level."
authors: ["borb","loren"]
---

This command adds an NPC character that hosts a bonus mission to the level.

# Context
{{ snippet hitandrun/command-contexts/level-init }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddNPCCharacterBonusMission( character, skeleton, locator, bonus_mission, drawable, conversation, no_replay, [completed_drawable] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddNPCCharacterBonusMission( character, skeleton, locator, bonus_mission, drawable, conversation, no_replay, [completed_drawable] )
```
{{ endtab }}
{{ endtabs }}

* **character**: The [internal name of the character](/hitandrun/misc/characters.md) hosting the mission.
* **skeleton**: The skeleton and animation set that character will use.
* **locator**: The name of a [Type 3 Locator](/pure3d/chunk-types/chunk-3000005.md#this_types_type3) that the character will spawn on.
* **bonus_mission**: The bonus mission that the character is hosting.
	* sr1
	* sr2
	* sr3
	* gr1
	* bm1
* **drawable**: The name of the drawable floating above the character's head when their mission has not been completed yet.
* **conversation**: The name of the dialogue conversation that will be used when talking to the character.
	* When the **mission** is "gr1", there is no conversation.
* **no_replay**: Disallows replaying the mission until the level is fully reloaded.
* **completed_drawable**: The name of the drawable floating above the character's head when their mission has been completed.
    * Optional, defaults to **drawable**.

There are various nuances to these arguments depending on what **mission** is set. Please see the [Notes](#notes) section for more details.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Street Race NPCs
// Replayable, "checkeredfinish" drawable when completed
AddNPCCharacterBonusMission("milhouse", "npd", "sr1_mhouse_sd", "sr1", "checkered", "intro", 0, "checkeredfinish");
AddNPCCharacterBonusMission("nelson", "npd", "sr2_nelson_sd", "sr2", "checkered", "intro", 0, "checkeredfinish");
AddNPCCharacterBonusMission("ralph", "npd", "sr3_ralph_sd", "sr3", "checkered", "intro", 0, "checkeredfinish");

// Wager Race NPC
// Replayable, no completed drawable (see Notes)
AddNPCCharacterBonusMission("louie", "npd", "sr4_louie_sd", "gr1", "dice", "intro", 0);

// Bonus Mission NPC
// Not replayable, "exclamation_shadow" drawable when completed
AddNPCCharacterBonusMission("cletus", "npd", "bm1_cletus_sd", "bm1", "exclamation", "jug", 1, "exclamation_shadow");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Street Race NPCs
-- Replayable, "checkeredfinish" drawable when completed
Game.AddNPCCharacterBonusMission("milhouse", "npd", "sr1_mhouse_sd", "sr1", "checkered", "intro", 0, "checkeredfinish")
Game.AddNPCCharacterBonusMission("nelson", "npd", "sr2_nelson_sd", "sr2", "checkered", "intro", 0, "checkeredfinish")
Game.AddNPCCharacterBonusMission("ralph", "npd", "sr3_ralph_sd", "sr3", "checkered", "intro", 0, "checkeredfinish")

-- Wager Race NPC
-- Replayable, no completed drawable (see Notes)
Game.AddNPCCharacterBonusMission("louie", "npd", "sr4_louie_sd", "gr1", "dice", "intro", 0)

-- Bonus Mission NPC
-- Not replayable, "exclamation_shadow" drawable when completed
Game.AddNPCCharacterBonusMission("cletus", "npd", "bm1_cletus_sd", "bm1", "exclamation", "jug", 1, "exclamation_shadow")
```
{{ endtab }}
{{ endtabs }}

# Notes
## When the "mission" is "sr1" or "sr2" {{ id street-races }}
When the **mission** argument is "sr1" or "sr2", a mod will need to require and configure the [Mod Launcher's](/lucasmodlauncher/intro.md) [Custom Bonus Mission Support](/lucasmodlauncher/hacks/custom-bonus-mission-support.md) hack to change the **character** from "milhouse" or "nelson" respectively.

## When the "mission" is "bm1" {{ id bonus-missions }}
By default when the **mission** is set to "bm1" and the bonus mission has been completed, the character will despawn once a vehicle they drive is called at a phone booth and they will no longer spawn on level load.

The [Mod Launcher's](/lucasmodlauncher/intro.md) [Replayable Bonus Missions](/lucasmodlauncher/hacks/replayable-bonus-missions.md) hack can be used to prevent this behaviour.

## When the "mission" is "gr1" {{ id wager-races }}
These types of missions do not have conversations so the **conversation** argument is ignored.

These types of missions are also not marked as completed in the usual sense so the **completed_drawable** argument is also ignored.