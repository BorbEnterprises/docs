---
title: "SetObjCameraName / SetObjMulticontName"
description: "Set the name of the camera and multi controller to use for a camera objective."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the name of the camera and multi controller to use for a [[../MissionObjectives/camera.md]].

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

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