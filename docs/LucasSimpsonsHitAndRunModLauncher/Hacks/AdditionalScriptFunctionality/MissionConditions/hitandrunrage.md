---
title: "hitandrunrage"
description: "Fail the player if they reach the part of the Hit & Run meter where it starts blinking red."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
---

Fail the player if they reach the part of the Hit & Run meter where it starts blinking red.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("hitandrunrage");

CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("hitandrunrage")

Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}