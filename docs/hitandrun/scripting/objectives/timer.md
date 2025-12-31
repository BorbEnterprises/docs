---
title: timer
description: This objective will wait for the number of seconds specified before moving on to the next stage.
authors: ["Colou"]
---

This objective will wait for the number of seconds specified before moving on to the next stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("timer");
	// Required: Specify the number of seconds the game will wait for.
	SetDurationTime(2);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("timer")
	-- Required: Specify the number of seconds the game will wait for.
	Game.SetDurationTime(2)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.
