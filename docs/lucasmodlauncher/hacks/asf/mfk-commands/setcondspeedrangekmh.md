---
title: SetCondSpeedRangeKMH
description: "Set a speed range for maintainspeed conditions."
summary:
    initialVersion: "1.18"
---

Set a speed range for [maintainspeed conditions](../conditions/maintainspeed.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-condition }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondSpeedRangeKMH( lower_limit, upper_limit );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondSpeedRangeKMH( lower_limit, upper_limit )
```
{{ endtab }}
{{ endtabs }}

* **lower_limit**: The lowest speed the player is allowed to go.
	* You can use `0` to have no lower limit.
* **upper_limit**: The highest speed the player is allowed to go.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("maintainspeed");
	SetCondSpeedRangeKMH(90, 150);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("maintainspeed")
	Game.SetCondSpeedRangeKMH(90, 150)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.