---
title: hitandrunrage
description: "Fail the player if they reach the part of the Hit & Run meter where it starts blinking red."
summary:
    initialVersion: "1.18"
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

# Notes
No additional notes.

# Version History
## 1.18
Added this condition type.