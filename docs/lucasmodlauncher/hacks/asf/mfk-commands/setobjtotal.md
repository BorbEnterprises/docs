---
title: SetObjTotal
description: "Set the total amount required for various ASF objectives."
summary:
    initialVersion: "1.18"
---

Set the total amount required for [collectcoins](../objectives/collectcoins.md), [collectwrench](../objectives/collectwrench.md), [completedwasps](../objectives/completedwasps.md), [destroycars](../objectives/destroycars.md), [event](../objectives/event.md), [hitpeds](../objectives/hitpeds.md) and [jump](../objectives/jump.md) objectives.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjTotal( total );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjTotal( total )
```
{{ endtab }}
{{ endtabs }}

* **total**: The total amount required to pass the objective.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("jump");
	// Jump 3 times
	SetObjTotal(3);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("jump")
	-- Jump 3 times
	Game.SetObjTotal(3)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.