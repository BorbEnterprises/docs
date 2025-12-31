---
title: SetStageHitAndRun
description: "Set the value of the Hit & Run meter when starting the stage."
summary:
    initialVersion: "1.18"
---

Set the value of the Hit & Run meter when starting the stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageHitAndRun( meter );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageHitAndRun( meter )
```
{{ endtab }}
{{ endtabs }}

meter: The value to set the meter to. From 0 to 100.
100 will trigger a Hit & Run when reaching the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	SetStageHitAndRun(100);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.SetStageHitAndRun(100)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.