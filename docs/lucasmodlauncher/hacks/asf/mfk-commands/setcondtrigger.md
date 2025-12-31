---
title: SetCondTrigger
description: "Specify the locator whose triggers will be used for the insidetrigger/outsidetrigger conditions."
summary:
    initialVersion: "1.18"
---

Specify the locator whose triggers will be used for the [insidetrigger/outsidetrigger conditions](../conditions/insidetrigger-outsidetrigger.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-condition }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondTrigger( locator_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondTrigger( locator_name )
```
{{ endtab }}
{{ endtabs }}

* **locator_name**: The name of the locator whose triggers will be used for the condition.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("insidetrigger");
	SetCondTrigger("z2phone1");
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("insidetrigger")
	Game.SetCondTrigger("z2phone1")
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.