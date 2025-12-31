---
title: hitandrunrage
description: "This type of objective requires the player to fill the Hit & Run meter to the point where it starts blinking red to pass the stage."
summary:
    initialVersion: "1.18"
---

This type of objective requires the player to fill the Hit & Run meter to the point where it starts blinking red to pass the stage.

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
Added this objective type.