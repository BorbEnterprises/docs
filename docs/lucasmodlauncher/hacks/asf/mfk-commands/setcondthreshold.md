---
title: SetCondThreshold
description: "Set a threshold for the insidetrigger / outsidetrigger conditions."
summary:
    initialVersion: "1.18"
---

Set a threshold for the [insidetrigger / outsidetrigger conditions](../conditions/insidetrigger-outsidetrigger.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-condition }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondThreshold( threshold );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondThreshold( threshold )
```
{{ endtab }}
{{ endtabs }}

* **threshold**: The amount of time the player must be inside or outside the trigger to fail the condition.
    * Defaults to 0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("insidetrigger");
	SetCondTrigger("z2phone1");

	// Fail the player if they're inside the trigger for 10 seconds.
	SetCondThreshold(10);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("insidetrigger")
	Game.SetCondTrigger("z2phone1")

	-- Fail the player if they're inside the trigger for 10 seconds.
	Game.SetCondThreshold(10)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.