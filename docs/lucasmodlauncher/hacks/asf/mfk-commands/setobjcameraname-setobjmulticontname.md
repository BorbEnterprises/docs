---
title: SetObjCameraName / SetObjMulticontName
description: "Set the name of the camera and multi controller to use for a camera objective."
summary:
    initialVersion: "1.18"
---

Set the name of the camera and multi controller to use for a [camera objective](../objectives/camera.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjCameraName( camera_name );
SetObjMulticontName( multicontroller_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjCameraName( camera_name )
Game.SetObjMulticontName( multicontroller_name )
```
{{ endtab }}
{{ endtabs }}

* **camera_name**: The name of the camera to use for the objective.
* **multicontroller_name**: The name of the camera multi controller to use for the objective.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("camera");
	// Set the camera and multi controller name.
	SetObjCameraName("mission0camShape");
	SetObjMulticontName("mission0cam");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("camera")
	-- Set the camera and multi controller name.
	Game.SetObjCameraName("mission0camShape")
	Game.SetObjMulticontName("mission0cam")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.