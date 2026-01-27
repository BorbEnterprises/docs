---
title: "spring"
description: "This type of objective requires the player to bounce on a spring (like an air vent) to pass the stage."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
---

This type of objective requires the player to bounce on a spring (like an air vent) to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("spring");

CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("spring")

Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}