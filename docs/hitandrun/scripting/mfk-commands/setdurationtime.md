---
title: SetDurationTime
description: "This command is used inside a timer objective to specify how long it should last."
authors: ["UnknownSteel", "legomariofanatic"]
---

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

Additionally, it must be a `timer` objective.

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddObjective("timer");
		SetDurationTime( time );
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.AddObjective("timer")
		Game.SetDurationTime( time )
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

* **time**: The duration (in seconds) that the stage should last.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();

	AddObjective("timer");
	
		// This stage will complete after 5 seconds have passed.
		SetDurationTime(5);
	
	CloseObjective();

CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()

	Game.AddObjective("timer")
		
		-- This stage will complete after 5 seconds have passed.
		Game.SetDurationTime(5)
	
	Game.CloseObjective()

Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
This command is modified by the Additional Script Functionality hack to have expanded functionality.

See [Modified Commands](/lucasmodlauncher/hacks/asf/modified-commands.md#setdurationtime) for more information.
