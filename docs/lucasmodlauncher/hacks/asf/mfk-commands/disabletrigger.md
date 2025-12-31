---
title: DisableTrigger
description: "Disable a locator's trigger(s) for a stage. Repeat for each locator's triggers you'd like to disable."
summary:
    initialVersion: "1.18"
---

Disable a locator's trigger(s) for a stage. Repeat for each locator's triggers you'd like to disable.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
DisableTrigger( locator_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.DisableTrigger( locator_name )
```
{{ endtab }}
{{ endtabs }}

* **locator_name**: The name of a locator whose triggers will be disabled.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	DisableTrigger("z2phone1");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.DisableTrigger("z2phone1")

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