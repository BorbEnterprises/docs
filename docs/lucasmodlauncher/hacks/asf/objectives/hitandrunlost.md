---
title: hitandrunlost
description: "This type of objective requires the player to lose their Hit & Run to pass the stage."
summary:
    initialVersion: "1.18"
---

This type of objective requires the player to lose their Hit & Run to pass the stage.

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
This objective type is only completed if the player loses their Hit & Run *without* getting caught.

# Version History
## 1.18
Added this objective type.