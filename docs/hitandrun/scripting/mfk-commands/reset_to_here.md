---
title: RESET_TO_HERE
description: "Tells the game to start at this stage when selecting the mission or restarting it."
---

This command tells the game to start at this stage when selecting the mission or restarting it.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
RESET_TO_HERE();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.RESET_TO_HERE()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
    RESET_TO_HERE();

    AddObjective("dummy");
    CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
    Game.RESET_TO_HERE()

    Game.AddObjective("dummy")
    Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.