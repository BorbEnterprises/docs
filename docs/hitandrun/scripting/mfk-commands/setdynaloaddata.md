---
title: SetDynaLoadData
description: Tells the game which zones to load upon restarting a mission.
authors: ["colou","loren"]
---

Tells the game which zones to load upon restarting a mission.

# Context
{{ snippet hitandrun/command-contexts/mission-init-root }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetDynaLoadData( dyna_load_data_string );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetDynaLoadData( dyna_load_data_string )
```
{{ endtab }}
{{ endtabs }}

* **dyna_load_data_string**: A [dyna load data string](/hitandrun/misc/dyna-load-data.md) that will be executed when the mission loads.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	...
	
	SetDynaLoadData("l1z1.p3d;l1r1.p3d;l1r7.p3d;");

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
	
	Game.SetDynaLoadData("l1z1.p3d;l1r1.p3d;l1r7.p3d;")

	Game.AddStage() 	
		...	
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
At least one zone must be loaded by the command, otherwise the game will hang on the loading screen. Attempting to put **SetDynaLoadData("");** will crash the game.
