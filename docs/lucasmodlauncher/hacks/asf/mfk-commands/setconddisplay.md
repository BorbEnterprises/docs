---
title: SetCondDisplay
description: "Set how any ASF condition displays to the user."
summary:
    initialVersion: "1.18"
---

Set how any ASF condition displays to the user.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-condition }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondDisplay( display_type );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondDisplay( display_type )
```
{{ endtab }}
{{ endtabs }}

## In any ASF Condition

* **display_type**: The type of display to use to convey (or hide) the condition to the player. 
    * **none**: The display will be hidden.

## In maintainSpeed Conditions

* **display_type**: The type of display to use to convey (or hide) the condition to the player.
    * **fill**: The bar will be full when the player is near the midpoint of the specified speed range.
    * **midpoint**: The bar will be empty when the player is near the lower limit and full when the player is near the higher limit.
        * Default.
    * **none**: The display will be hidden.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("hitpeds");
	SetCondDisplay("none");
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("hitpeds")
	Game.SetCondDisplay("none")
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18.1
Added the "none" display mode that works on all ASF conditions.

## 1.18
Added this command.