---
title: SetObjDecay
description: "Set the decay delay and decay rate for the insidetrigger / outsidetrigger objectives."
summary:
    initialVersion: "1.18"
---

Set the decay delay and decay rate for the [insidetrigger / outsidetrigger objectives](../objectives/insidetrigger-outsidetrigger.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjDecay( decay_rate, [decay_delay]  );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjDecay( decay_rate, [decay_delay]  )
```
{{ endtab }}
{{ endtabs }}

* **decay_rate**: The rate at which the objective decays. 
    * Defaults to 0.
* **decay_delay**: The amount of time that must pass before the objective begins decaying.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("insidetrigger");
	SetObjTrigger("z2Phone1");

	// Decay the meter by "3 seconds" when the player is not inside the trigger for more than 2 seconds.
	SetObjDecay(3, 2);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("insidetrigger")
	Game.SetObjTrigger("z2Phone1")

	-- Decay the meter by "3 seconds" when the player is not inside the trigger for more than 2 seconds.
	Game.SetObjDecay(3, 2)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.