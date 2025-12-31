---
title: SetStageHitAndRunDecayInterior
description: "Set the Hit & Run decay rate while in an interior for a stage."
summary:
    initialVersion: "1.18"
---

Set the Hit & Run decay rate while in an interior for a stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageHitAndRunDecayInterior( decay_rate );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageHitAndRunDecayInterior( decay_rate )
```
{{ endtab }}
{{ endtabs }}

* **decay_rate**: The decay rate. Defaults to the level's interior decay rate.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();    
	SetStageHitAndRunDecayInterior(4.0);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	Game.SetStageHitAndRunDecayInterior(4.0)

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