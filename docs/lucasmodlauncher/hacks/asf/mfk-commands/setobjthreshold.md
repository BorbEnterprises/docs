---
title: SetObjThreshold
description: "Set a threshold for the insidetrigger / outsidetrigger objectives."
summary:
    initialVersion: "1.18"
---

Set a threshold for the [insidetrigger / outsidetrigger objectives](../objectives/insidetrigger-outsidetrigger.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

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

* **threshold**: The amount of time the player must be inside or outside the trigger to pass the objective.
    * Defaults to 0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("insidetrigger");
	SetObjTrigger("z2phone1");

	// Require the player to be inside that trigger for 10 seconds to pass.
	SetObjThreshold(10);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("insidetrigger")
	Game.SetObjTrigger("z2phone1")

	-- Require the player to be inside that trigger for 10 seconds to pass.
	Game.SetObjThreshold(10)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.