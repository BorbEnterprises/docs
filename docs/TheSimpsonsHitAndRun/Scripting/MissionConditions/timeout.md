---
title: "timeout"
description: "Fails the player if they run out of time in a stage."
authors: [ 2 ]
---

This type of condition fails the player if they run out of time in the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	SetStageTime(10);

	AddObjective("dummy");
	CloseObjective();

	// Fail the player if they take longer than 10 seconds on this stage
	AddCondition("timeout");
	CloseCondition();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.SetStageTime(10)

	Game.AddObjective("dummy")
	Game.CloseObjective()

	-- Fail the player if they take longer than 10 seconds on this stage
	Game.AddCondition("timeout")
	Game.CloseCondition()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
This condition will immediately fail the player if the stage doesn't call [[../ConsoleCommands/SetStageTime.md]] or [[../ConsoleCommands/AddStageTime.md]].