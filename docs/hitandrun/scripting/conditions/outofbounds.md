---
title: outofbounds
description: "Fails the player if they enter a Type 0 Locator with Event 4. (death trigger)"
authors: ["Gordon_CMB"]
---

This type of condition fails the player if they enter a Type 0 Locator with Event 4. (death trigger) The player is not failed immediately upon entering the death trigger, but rather after the screen fades and the player character respawns.

# Context

{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Examples

{{ tabs }}
{{ tab MFK }}
```js
AddStage();
    AddObjective("dummy");
    CloseObjective();
    AddCondition("outofbounds"); // Fails the player after they're reset following entry of a death trigger. 
    CloseCondition();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
AddStage()
    AddObjective("dummy")
    CloseObjective()
    AddCondition("outofbounds") -- Fails the player after they're reset following entry of a death trigger. 
    CloseCondition()
CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
Radical doesn't use this condition in any of their scripts, but it is in fact fully functional. 
