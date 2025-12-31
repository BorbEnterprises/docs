---
title: AddCondTargetModel
description: "Specify the name of a valid model for a destroycars condition or a hitpeds condition."
summary:
    initialVersion: "1.18"
---

Specify the name of a valid model for a [destroycars condition](../conditions/destroycars.md) or a [hitpeds condition](../conditions/hitpeds.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-condition }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddCondTargetModel( model_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondTargetModel( model_name )
```
{{ endtab }}
{{ endtabs }}

* **model_name**: The name of the car or character model (depending on the condition type).

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("hitpeds");
	AddCondTargetModel("marge");
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("hitpeds")
	Game.AddCondTargetModel("marge")
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.