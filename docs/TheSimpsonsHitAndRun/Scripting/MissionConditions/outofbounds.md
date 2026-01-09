---
title: "outofbounds"
description: "Fails the player if they enter a death trigger."
authors: [ 2, 104 ]
---

This type of condition fails the player if they enter a death trigger.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
    AddObjective("dummy");
    CloseObjective();

    AddCondition("outofbounds");
    CloseCondition();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
   	Game.AddObjective("dummy")
    Game.CloseObjective()

    Game.AddCondition("outofbounds")
    Game.CloseCondition()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
This condition type is never used in the base game.