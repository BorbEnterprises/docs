---
title: SetStageHitAndRunDecayHitAndRun
description: "Set the Hit & Run meter decay rate while in a Hit & Run for a stage."
summary:
    initialVersion: "1.18"
---

Set the Hit & Run meter decay rate while in a Hit & Run for a stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageHitAndRunDecayHitAndRun( decay_rate );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageHitAndRunDecayHitAndRun( decay_rate )
```
{{ endtab }}
{{ endtabs }}

* **decay_rate**: The decay rate. Defaults to the level's Hit & Run decay rate.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();    
	SetStageHitAndRunDecayHitAndRun(4.0);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.SetStageHitAndRunDecayHitAndRun(4.0)

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