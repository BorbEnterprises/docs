---
title: SetInitialWalk
description: Sets a Type 3 Locator that the player character will automatically walk towards when the mission is selected or restarted.
authors: ["colou"]
---

Sets a [Type 3 Locator](/pure3d/chunk-types/chunk-3000005.md#this_types_type3) that the player character will automatically walk towards when the mission is selected or restarted.

# Context
{{ snippet hitandrun/command-contexts/mission-init-root }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetInitialWalk( walk_locator );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetInitialWalk( walk_locator )
```
{{ endtab }}
{{ endtabs }}

* **walk_locator**: The [Type 3 Locator](/pure3d/chunk-types/chunk-3000005.md#this_types_type3) that the player will walk to.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	...
	
	SetInitialWalk("level1_homer_walkto");
	
	AddStage();
		...
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")
	...
	
	Game.SetInitialWalk("level1_homer_walkto")
	
	Game.AddStage()
		...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.
