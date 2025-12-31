---
title: SetObjUseCameraPosition
description: "Set whether or not the game should use the camera's position for spawning traffic and pedestrians during a camera objective."
summary:
    initialVersion: "1.18"
---

Set whether or not the game should use the camera's position for spawning traffic and pedestrians during a [camera objective](../objectives/camera.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjUseCameraPosition( use_camera_position );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjUseCameraPosition( use_camera_position )
```
{{ endtab }}
{{ endtabs }}

* **use_camera_position**: Set whether or not to use the camera position. 
    * Defaults to 0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("camera");
	SetObjCameraName("mission0camShape");
	SetObjMulticontName("mission0cam");

	SetObjUseCameraPosition(0);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("camera")
	Game.SetObjCameraName("mission0camShape")
	Game.SetObjMulticontName("mission0cam")

	Game.SetObjUseCameraPosition(0)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.