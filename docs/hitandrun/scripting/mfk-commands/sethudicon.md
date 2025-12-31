---
title: SetHUDIcon
description: "This command sets the HUD icon to use in a stage."
authors: ["legomariofanatic"]
---

{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetHUDIcon( icon_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHUDIcon( icon_name )
```
{{ endtab }}
{{ endtabs }}

* **icon_name**: The name of the sprite to use as a HUD icon.
* * If the `p3d` file containing this sprite is not loaded when the stage is reached, then no HUD icon will be used.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m3");
	...
	AddStage();
		SetHUDIcon("simpsons");
		AddObjective("dummy");
			...
		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")
	...
	Game.AddStage()
		Game.SetHUDIcon("simpsons")
		Game.AddObjective("dummy")
			...
		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.
