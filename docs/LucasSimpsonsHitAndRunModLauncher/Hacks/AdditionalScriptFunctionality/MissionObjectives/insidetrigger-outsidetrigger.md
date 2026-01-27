---
title: "insidetrigger / outsidetrigger"
description: "These types of objectives require the player to be either inside or outside the specified triggers to pass the stage."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
---

These types of objectives require the player to be either inside or outside the specified triggers to pass the stage.

# Examples
## insidetrigger
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("insidetrigger");
	// Specify a locator whose triggers the player must be inside to advance the objective.
	SetObjTrigger("z2phone1");
	
	// Specify the threshold for passing the stage. Optional.
	SetObjThreshold(10);

	// Set a message to show when inside the trigger. Optional.
	SetObjMessageIndex(3);
	
	// Specify the decay of the meter when the player is not inside any of the triggers. Optional.
	SetObjDecay(3, 2);
	
	// Specify the sound that will play when entering any of the triggers. Optional.
	SetObjSound("gag_alm2", "enter_trigger");
	
	// Specify the sound that will play when staying inside any of the triggers. Optional.
	SetObjSound("countdown_beeps", "inside_trigger", 1, 5);
	
	// Specify the sound that will play when exiting the triggers. Optional.
	SetObjSound("P_HitByC_Mrg_01", "exit_trigger");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("insidetrigger")
	-- Specify a locator whose triggers the player must be inside to advance the objective.
	Game.SetObjTrigger("z2phone1")
	
	-- Specify the threshold for passing the stage. Optional.
	Game.SetObjThreshold(10)

	-- Set a message to show when inside the trigger. Optional.
	Game.SetObjMessageIndex(3)
	
	-- Specify the decay of the meter when the player is not inside any of the triggers. Optional.
	Game.SetObjDecay(3, 2)
	
	-- Specify the sound that will play when entering any of the triggers. Optional.
	Game.SetObjSound("gag_alm2", "enter_trigger")
	
	-- Specify the sound that will play when staying inside any of the triggers. Optional.
	Game.SetObjSound("countdown_beeps", "inside_trigger", 1, 5)
	
	-- Specify the sound that will play when exiting the triggers. Optional.
	Game.SetObjSound("P_HitByC_Mrg_01", "exit_trigger");
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

## outsidetrigger
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("outsidetrigger");
	// Specify a locator whose triggers the player must be outside to advance the objective.
	SetObjTrigger("z2phone1");

	// This objective is largely the same except you use "outside_trigger" to specify the sound when you're outside.
	// You can only have an "outside_trigger" sound on an "outsidetrigger" stage.
	SetObjSound("countdown_beeps", "outside_trigger", 1, 5);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("outsidetrigger")
	-- Specify a locator whose triggers the player must be outside to advance the objective.
	Game.SetObjTrigger("z2phone1")

	-- This objective is largely the same except you use "outside_trigger" to specify the sound when you're outside.
	-- You can only have an "outside_trigger" sound on an "outsidetrigger" stage.
	Game.SetObjSound("countdown_beeps", "outside_trigger", 1, 5)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}