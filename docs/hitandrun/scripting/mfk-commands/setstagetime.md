---
title: SetStageTime
description: "This command sets the stage time for the stage."
authors: ["legomariofanatic"]
---


# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageTime( time_limit );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageTime( time_limit )
```
{{ endtab }}
{{ endtabs }}

* **time_limit**: The amount of time (in seconds) to set the stage timer to.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	...
	AddStage();
		SetStageTime(60);	// Sets the stage timer to 60 seconds for this stage.
	
		AddObjective("dummy");
	
		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1");
	...
	Game.AddStage();
		Game.SetStageTime(60);	-- Sets the stage timer to 60 seconds for this stage.
	
		Game.AddObjective("dummy");
	
		Game.CloseObjective();
	Game.CloseStage();
Game.CloseMission();
```
{{ endtab }}
{{ endtabs }}

# Notes
It is recommended that you use a [timeout](/hitandrun/scripting/conditions/timeout.md) condition with SetStageTime. However, this is not required; if the player runs out of time without a timeout condition, then the timer will simply disappear with no consequence.
