---
title: "camera"
description: "This type of objective allows you to play a camera for the stage."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
---

This type of objective allows you to play a camera for the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("camera");
	// Required: Set the camera and multi controller name.
	SetObjCameraName("mission0camShape");
	SetObjMulticontName("mission0cam");

	// Optional: Set whether or not the user can skip the camera animation. Defaults to 0.
	SetObjCanSkip(0);

	// Optional: Set whether or not there will be letterboxing when the camera is playing. Defaults to 0.
	SetObjNoLetterbox(0);

	// Optional: Set whether or not the game will act as though the player is at the camera's position during the objective. Defaults to 0.
	SetObjUseCameraPosition(0);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("camera")
	-- Required: Set the camera and multi controller name.
	Game.SetObjCameraName("mission0camShape")
	Game.SetObjMulticontName("mission0cam")

	-- Optional: Set whether or not the user can skip the camera animation. Defaults to 0.
	Game.SetObjCanSkip(0)

	-- Optional: Set whether or not there will be letterboxing when the camera is playing. Defaults to 0.
	Game.SetObjNoLetterbox(0)

	-- Optional: Set whether or not the game will act as though the player is at the camera's position during the objective. Defaults to 0.
	Game.SetObjUseCameraPosition(0)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}