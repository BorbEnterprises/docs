---
title: SetStageHitAndRunFine
description: "Set the Hit & Run fine for a stage."
summary:
    initialVersion: "1.18"
---

Set the Hit & Run fine for a stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageHitAndRunFine( fine );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageHitAndRunFine( fine )
```
{{ endtab }}
{{ endtabs }}

* **fine**: The amount to fine the player during the stage. Default's to the level's hit & run fine.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// No fine during this stage, go crazy.
	SetStageHitAndRunFine(0);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	-- No fine during this stage, go crazy.
	Game.SetStageHitAndRunFine(0)

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