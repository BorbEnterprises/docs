---
title: "hitandrun"
description: "This type of objective requires the player to get a Hit & Run to pass the stage."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
---

This type of objective requires the player to get a Hit & Run to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("hitandrun");

CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("hitandrun")

Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}