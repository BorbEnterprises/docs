---
title: SetObjNoLetterbox
description: "Set whether or not there will be letterboxing."
summary:
    initialVersion: "1.18"
---

Set whether or not there will be [letterboxing](https://en.wikipedia.org/wiki/Letterboxing_(filming)) during a [camera objective](../objectives/camera.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjNoLetterbox( no_letterbox );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjNoLetterbox( no_letterbox )
```
{{ endtab }}
{{ endtabs }}

* **no_letterbox**: Whether or not to have no letterbox. Defaults to 0.  

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("camera");
	SetObjCameraName("mission0camShape");
	SetObjMulticontName("mission0cam");

	// Disable the letterbox during this camera.
	SetObjNoLetterbox(1);
CloseObjective();  
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("camera")
	Game.SetObjCameraName("mission0camShape")
	Game.SetObjMulticontName("mission0cam")

	-- Disable the letterbox during this camera.
	Game.SetObjNoLetterbox(1)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.