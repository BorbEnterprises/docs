---
title: "hitandrunlost"
description: "Fail the player if they lose their Hit & Run."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 380 # 1.18.1
---

Fail the player if they lose their Hit & Run. 

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("hitandrunlost");

CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("hitandrunlost")

Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
This condition type only fails the player if they lose their Hit & Run *without* getting caught.