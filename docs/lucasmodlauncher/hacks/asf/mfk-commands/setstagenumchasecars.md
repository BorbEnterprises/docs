---
title: SetStageNumChaseCars
description: "Set the amount of chase cars that will spawn during a Hit & Run this stage."
summary:
    initialVersion: "1.18"
---

Set the amount of chase cars that will spawn during a Hit & Run this stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageNumChaseCars( amount );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageNumChaseCars( amount )
```
{{ endtab }}
{{ endtabs }}

* **amount**: The amount of chase cars to spawn. This can be from 1 to 5. Defaults to the level's number of chase cars.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// You probably want to avoid stuff during this stage...
	SetStageNumChaseCars(5);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	-- You probably want to avoid stuff during this stage...
	Game.SetStageNumChaseCars(5)

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