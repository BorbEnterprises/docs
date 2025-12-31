---
title: hitandruncaught
description: "This type of objective requires the player to get caught in a Hit & Run to pass the stage."
summary:
    initialVersion: "1.18"
---

This type of objective requires the player to get caught in a Hit & Run to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("hitandruncaught");

CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("hitandruncaught")

Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
You may want to use [SetStageHitAndRunFine](../mfk-commands/setstagehitandrunfine.md) to make this type of objective more fair for the player since you're forcing them to get caught.

# Version History
## 1.18
Added this objective type.