---
title: "maintainspeed"
description: "Fail the player if they do not maintain a speed within a specified range during the stage."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
---

Fail the player if they do not maintain a speed within a specified range during the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("maintainspeed");
	// Required: Specify the range the player must keep their speed within during the stage.
	SetCondSpeedRangeKMH(90, 150);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("maintainspeed")
	-- Required: Specify the range the player must keep their speed within during the stage.
	Game.SetCondSpeedRangeKMH(90, 150)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}