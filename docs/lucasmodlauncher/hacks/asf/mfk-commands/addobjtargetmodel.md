---
title: AddObjTargetModel
description: "Specify the name of a valid model for a destroycars objective or a hitpeds objective."
summary:
    initialVersion: "1.18"
---

Specify the name of a valid model for a [destroycars objective](../objectives/destroycars.md) or a [hitpeds objective](../objectives/hitpeds.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddObjTargetModel( model_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjTargetModel( model_name )
```
{{ endtab }}
{{ endtabs }}

* **model_name**: The name of the car or character model (depending on the objective type).

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("hitpeds");
	AddObjTargetModel("marge");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("hitpeds")
	Game.AddObjTargetModel("marge")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.