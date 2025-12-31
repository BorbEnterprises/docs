---
title: SetStageCarChangeHitAndRunChange
description: "Set the amount the Hit & Run meter will change when swapping to a different vehicle for the stage."
summary:
    initialVersion: "1.18"
---

Set the amount the Hit & Run meter will change when swapping to a different vehicle for the stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageCarChangeHitAndRunChange( change_amount );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageCarChangeHitAndRunChange( change_amount )
```
{{ endtab }}
{{ endtabs }}

* **change_amount**: The amount that will be added to the Hit & Run meter when changing your car. 
	* Defaults to -100.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();    
	SetStageCarChangeHitAndRunChange(-100);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()    
	Game.SetStageCarChangeHitAndRunChange(-100)

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