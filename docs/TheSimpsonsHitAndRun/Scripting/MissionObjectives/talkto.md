---
title: "talkto"
description: "This type of objective requires the player to interact with an NPC with an exclamation mark overhead to pass the stage."
authors: [ 104, 27739 ]
---

This type of objective requires the player to interact with an NPC with an exclamation mark overhead to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// The player must talk to Marge to pass the objective.
AddObjective("talkto");
	AddNPC("marge", "m1_marge_sd"); // Places Marge at the Type 3 Locator named "m1_marge_sd".
	AddObjectiveNPCWaypoint( "marge", "marge_walk_1" ); // Sets a Type 3 Locator for the NPC to walk towards.
	SetTalkToTarget("marge", 0, 0.2);
	// The first argument is the drawable used:
	// - 0 is the standard exclamation mark
	// - 1 is a drawable named "gift"
	// - 2 is a drawable named "interior_icon"
	// The second argument is a height offset.
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
-- The player must talk to Marge to pass the objective.
Game.AddObjective("talkto")
	Game.AddNPC("marge", "m1_marge_sd") -- Places Marge at the Type 3 Locator named "m1_marge_sd".
	Game.AddObjectiveNPCWaypoint( "marge", "marge_walk_1" ) -- Sets a Type 3 Locator for the NPC to walk towards.
	Game.SetTalkToTarget("marge", 0, 0.2)
	-- The first argument is the drawable used:
	-- - 0 is the standard exclamation mark
	-- - 1 is a drawable named "gift"
	-- - 2 is a drawable named "interior_icon"
	-- The second argument is a height offset.
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
* Radical generally uses these stages before dialogue stages, but the dialogue stage isn't strictly necessary.
* The NPC will walk back and forth between the Locators specified in [[../ConsoleCommands/AddObjectiveNPCWaypoint.md]] and AddNPC provided the player character is far enough away.
  * When the player character gets close, NPCs will stop and look in the player's direction.
  * If more than one call to AddObjectiveNPCWaypoint is present, the NPC will walk through the Locators in sequence before returning to the Locator specified in AddNPC.
* The extra values in [[../ConsoleCommands/SetTalkToTarget.md]] default to zero, meaning they are not strictly required.
  * Radical offsets the icon with certain characters for aesthetic purposes.