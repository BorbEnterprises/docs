---
title: SetHUDMapDrawable
description: "Set the current drawable for the HUD map when a mission starts."
summary:
    initialVersion: "1.18"
---

Set the current drawable for the HUD map when a mission starts.

# Context
{{ snippet hitandrun/command-contexts/mission-init-root }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetHUDMapDrawable( drawable_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHUDMapDrawable( drawable_name )
```
{{ endtab }}
{{ endtabs }}

* **drawable_name**: The name of the drawable to use.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");

	...

    // This command should be used in the root of the mission.
	SetHUDMapDrawable("l4hudmapShape_alternate");

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

    -- This command should be used in the root of the mission.
	Game.SetHUDMapDrawable("l4hudmapShape_alternate")

	Game.AddStage()
    	...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes

* Meshes are the type of drawable intended for use as a HUD Map though some other types of drawables are also supported.
    * By default, the game stores the mesh for the HUD Map in `art\frontend\scrooby\resource\pure3d\lXhudmap.p3d`.
* This will not revert when the mission ends, it is up to the mod to put the HUD Map drawable back when necessary.

# Version History
## 1.18
Added this command.