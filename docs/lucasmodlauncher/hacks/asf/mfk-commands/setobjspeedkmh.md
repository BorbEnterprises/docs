---
title: SetObjSpeedKMH
description: "Set the speed required for a reachspeed objective."
summary:
    initialVersion: "1.18"
---

Set the speed required for a [reachspeed objective](../objectives/reachspeed.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjSpeedKMH( target_speed );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjSpeedKMH( target_speed )  
```
{{ endtab }}
{{ endtabs }}

* **target_speed**: The speed required for the objective.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("reachspeed");
	SetObjSpeedKMH(120);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("reachspeed")
	Game.SetObjSpeedKMH(120)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.