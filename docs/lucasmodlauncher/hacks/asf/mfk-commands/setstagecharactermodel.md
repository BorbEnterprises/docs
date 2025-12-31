---
title: SetStageCharacterModel
description: "Set the player character's model for the stage."
summary:
    initialVersion: "1.18"
---

Set the player character's model for the stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageCharacterModel( model, [animation_set] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageCharacterModel( model, [animation_set] )
```
{{ endtab }}
{{ endtabs }}

* **model**: The character model to use.
* **animation_set**: The animation set to use.
    * Optional, defaults to the current player character's animation set as of 1.19.
        * Using anything else can cause issues.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
    // Switch to Homer's Muumuu costume for the stage.
	SetStageCharacterModel("h_fat");

	AddObjective("dummy");
    
    CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
    -- Switch to Homer's Muumuu costume for the stage.
	Game.SetStageCharacterModel("h_fat")

	Game.AddObjective("dummy")
    
    Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.19
Updated to default the second argument to the player's current animation set instead of requiring the argument.

## 1.18.1
Fixed an issue where calling this command in a stage that calls [RESET_TO_HERE](/hitandrun/scripting/mfk-commands/reset_to_here.md) that is preceded by another stage that calls this command (with the same model and animation set) didn't work.

## 1.18
Added this command.