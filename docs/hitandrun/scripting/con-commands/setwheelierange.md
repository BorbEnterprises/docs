---
title: SetWheelieRange
description: "Sets the distance for which a vehicle will perform a wheelie when accelerating."
authors: ["borb"]
---

This command sets the distance for which a vehicle will perform a wheelie when accelerating. In order to perform a wheelie, the vehicle must be stopped or nearly stopped.

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieRange( range );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieRange( range )
```
{{ endtab }}
{{ endtabs }}

* **range**: Sets the distance for which a vehicle will perform a wheelie. When in this state, the vehicles's center of mass is offset to the values specified in [SetWheelieOffsetY](setwheelieoffsety.md), [SetWheelieOffsetZ](setwheelieoffsetz.md), and [SetWheelieOffsetX](/lucasmodlauncher/hacks/asf/con-commands/setwheelieoffsetx.md).

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieRange(0.3);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieRange(0.3)
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.