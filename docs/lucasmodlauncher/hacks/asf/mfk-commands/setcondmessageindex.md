---
title: SetCondMessageIndex
description: "Set a message index for the insidetrigger / outsidetrigger conditions."
summary:
    initialVersion: "1.18"
---

Set a message index for the [insidetrigger / outsidetrigger conditions](../conditions/insidetrigger-outsidetrigger.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-condition }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondMessageIndex( message_index );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondMessageIndex( message_index )
```
{{ endtab }}
{{ endtabs }}

* **message_index**: The condition message index (just like [SetStageMessageIndex](/hitandrun/scripting/mfk-commands/setstagemessageindex.md)) to use for the condition.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("insidetrigger");
	SetCondTrigger("z2phone1");

	// Show MISSION_OBJECTIVE_03 if the player enters the trigger.
	SetCondMessageIndex(3);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("insidetrigger")
	Game.SetCondTrigger("z2phone1")

	-- Show MISSION_OBJECTIVE_03 if the player enters the trigger.
	Game.SetCondMessageIndex(3)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.