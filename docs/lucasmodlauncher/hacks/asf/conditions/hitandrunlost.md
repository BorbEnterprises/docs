---
title: hitandrunlost
description: "Fail the player if they lose their Hit & Run."
summary:
    initialVersion: "1.18.1"
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

# Version History
## 1.18.1
Added this condition type.