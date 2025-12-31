---
title: SetCondDelay
description: "Specify a delay for the mission failed screen when failing various types of ASF conditions."
summary:
    initialVersion: "1.18"
---

Specify a delay for the mission failed screen when failing [collectcoins](../conditions/collectcoins.md), [collectwrench](../conditions/collectwrench.md), [destroycars](../conditions/destroycars.md), [hitandrun](../conditions/hitandrun.md), [hitandruncaught](../conditions/hitandruncaught.md), [hitandrunrage](../conditions/hitandrunrage.md), [hitpeds](../conditions/hitpeds.md), [jump](../conditions/jump.md) or [spring](../conditions/spring.md) conditions.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-condition }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondDelay( delay );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondDelay( delay )
```
{{ endtab }}
{{ endtabs }}

* **delay**: The amount of time in seconds to delay the mission ending after the condition is failed. 
    * Default delay varies by condition type.
    * [collectcoins](../conditions/collectcoins.md): 1 second.
    * [collectwrench](..//conditions/collectwrench.md): 1 second.
    * [destroycars](../conditions/destroycars.md): 1 second.
    * [hitandrun](../conditions/hitandrun.md): 2 seconds.
    * [hitandruncaught](../conditions/hitandruncaught.md): 2 seconds.
    * [hitandrunrage](../conditions/hitandrunrage.md): 1 second.
    * [hitpeds](../conditions/hitpeds.md): 1 second.
    * [jump](../conditions/jump.md): 1 second.
    * [spring](../conditions/spring.md): 1 second.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("jump");
	// Make it wait longer for some reason.
	SetCondDelay(3);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("jump")
	-- Make it wait longer for some reason.
	Game.SetCondDelay(3)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.