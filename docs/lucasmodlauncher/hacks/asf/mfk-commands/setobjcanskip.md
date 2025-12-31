---
title: SetObjCanSkip
description: Set whether or not a camera objective can be skipped.
summary:
    initialVersion: "1.18"
---

Set whether or not a [camera objective](../objectives/camera.md) can be skipped.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjCanSkip( can_skip );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjCanSkip( can_skip )
```
{{ endtab }}
{{ endtabs }}

* **can_skip** : Whether or not the player can skip the objective. 
    * Defaults to 0 / false.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("camera");
	SetObjCameraName("mission0camShape");
	SetObjMulticontName("mission0cam");

	// Let the player skip the camera animation.
	SetObjCanSkip(1);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("camera")
	Game.SetObjCameraName("mission0camShape")
	Game.SetObjMulticontName("mission0cam")

	-- Let the player skip the camera animation.
	Game.SetObjCanSkip(1)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18.1
Made ASF commands that take a boolean as an argument accept `true` or `false` as well as 0 or 1 instead of accepting any integer and treating it as true if it's not 0.

## 1.18
Added this command.