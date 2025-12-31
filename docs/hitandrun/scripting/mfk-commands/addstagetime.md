---
title: AddStageTime
description: "This command adds time to the stage timer."
authors: ["legomariofanatic"]
---

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddStageTime( time_limit );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStageTime( time_limit )
```
{{ endtab }}
{{ endtabs }}

* **time_limit**: The amount of time (in seconds) to add to the active stage timer.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	...
	AddStage();
	
		\\ Set the stage timer to 60 seconds here.
		SetStageTime(60);
		
		AddObjective("dummy");
		
		CloseObjective();
	
	CloseStage();
	
	AddStage();
	
		\\ Then add 30 seconds to the stage timer when reaching this stage.
		AddStageTime(30);
	
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
	
		-- Set the stage timer to 60 seconds here.
		Game.SetStageTime(60)
		
		Game.AddObjective("dummy")
		
		Game.CloseObjective()
	
	Game.CloseStage()
	
	Game.AddStage()
	
		-- Then add 30 seconds to the stage timer when reaching this stage.
		Game.AddStageTime(30)
	
		Game.AddObjective("dummy")
	
		Game.CloseObjective()
	
	Game.CloseStage()

Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
* It is recommended that you use a [timeout](/hitandrun/scripting/conditions/timeout.md) condition with AddStageTime. However, this is not required; if the player runs out of time without a timeout condition, then the timer will simply disappear with no consequence.
* If no active stage timer is present when reaching a stage that uses AddStageTime, then the game will treat the active stage timer as being 0 seconds.
* If `time_limit` is set to 0, then the game will add 1 second to the active stage timer when reaching the next stage, provided that contains AddStageTime.
* If `time_limit` is set to -1, then the game will not add any time to the active stage timer, and it will instead just carry over to the next stage, provided that contains AddStageTime.
