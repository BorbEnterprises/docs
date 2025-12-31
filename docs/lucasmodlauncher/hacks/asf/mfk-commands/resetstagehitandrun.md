---
title: ResetStageHitAndRun
description: "Resets the Hit & Run meter when reaching a stage, erasing all existing chase cars."
summary:
    initialVersion: "1.18"
---

Resets the Hit & Run meter when reaching a stage, erasing all existing chase cars.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
ResetStageHitAndRun();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.ResetStageHitAndRun()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	ResetStageHitAndRun();

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage();
	Game.ResetStageHitAndRun()

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