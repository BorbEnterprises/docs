---
title: camera
description: "This type of objective allows you to play a camera for the stage."
summary:
    initialVersion: "1.18"
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

# Notes
No additional notes.

# Version History
## 1.18
Added this objective type.