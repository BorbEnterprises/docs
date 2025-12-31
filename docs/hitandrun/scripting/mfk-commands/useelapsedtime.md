---
title: UseElapsedTime
description: "Makes a stage timer added with SetStageTime or AddStageTime count up rather than down."
authors: ["loren"]
---

This command makes a stage timer added with [SetStageTime](setstagetime.md) or [AddStageTime](addstagetime.md) count up rather than down.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
UseElapsedTime();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.UseElapsedTime()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	...

	AddStage();
		SetStageTime(0);
		UseElapsedTime(); // Make the timer count up from 0 in this stage

		AddObjective("dummy");

		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")
	...

	Game.AddStage()
		Game.SetStageTime(0)
		Game.UseElapsedTime() -- Make the timer count up from 0 in this stage

		Game.AddObjective("dummy")

		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
This is only used in conjunction with Wager Races in the original game but it can be used anywhere. Just note that outside of these missions, timers will flash red below 10 seconds even if they're counting up.