---
title: spring
description: "This type of objective requires the player to bounce on a spring (like an air vent) to pass the stage."
summary:
    initialVersion: "1.18"
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

# Notes
No additional notes.

# Version History
## 1.18
Added this objective type.