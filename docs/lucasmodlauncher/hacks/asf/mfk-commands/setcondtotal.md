---
title: SetCondTotal
description: "Set the total amount required to fail various ASF conditions."
summary:
    initialVersion: "1.18"
---

Set the total amount required to fail [collectcoins](../conditions/collectcoins.md), [collectwrench](../conditions/collectwrench.md), [destroycars](../conditions/destroycars.md), [event](../conditions/event.md), [hitpeds](../conditions/hitpeds.md) and [jump](../conditions/jump.md) conditions.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-condition }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondTotal( total );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondTotal( total )
```
{{ endtab }}
{{ endtabs }}

* **total**: The total amount required to fail the condition.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("jump");
	// Jump 3 times
	SetCondTotal(3);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("jump")
	-- Jump 3 times
	Game.SetCondTotal(3)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.