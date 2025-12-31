---
title: SetObjTrigger
description: "Specify the locator whose triggers will be used for the insidetrigger/outsidetrigger objectives."
summary:
    initialVersion: "1.18"
---

Specify the locator whose triggers will be used for the [insidetrigger/outsidetrigger objectives](../objectives/insidetrigger-outsidetrigger.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjTrigger( locator_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjTrigger( locator_name )
```
{{ endtab }}
{{ endtabs }}

* **locator_name**: The name of the locator whose triggers will be used for the objective.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("insidetrigger");
	SetObjTrigger("z2phone1");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("insidetrigger")
	Game.SetObjTrigger("z2phone1")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.