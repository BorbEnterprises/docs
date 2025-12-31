---
title: SetObjMessageIndex
description: "Set a message index for the insidetrigger / outsidetrigger objectives."
summary:
    initialVersion: "1.18"
---

Set a message index for the [insidetrigger / outsidetrigger objectives](../objectives/insidetrigger-outsidetrigger.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjMessageIndex( message_index );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjMessageIndex( message_index )
```
{{ endtab }}
{{ endtabs }}

* **message_index**: The objective message index (just like [SetStageMessageIndex](/hitandrun/scripting/mfk-commands/setstagemessageindex.md)) to use for the objective.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("insidetrigger");
	SetObjTrigger("z2phone1");

	// Show MISSION_OBJECTIVE_03 if the player enters the trigger.
	SetObjMessageIndex(3);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("insidetrigger")
	Game.SetObjTrigger("z2phone1")

	-- Show MISSION_OBJECTIVE_03 if the player enters the trigger.
	Game.SetObjMessageIndex(3)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.