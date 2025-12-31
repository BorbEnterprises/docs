---
title: SetWheelieOffsetY
description: "Sets the Y offset of the vehicle's center of mass when performing a wheelie."
authors: ["borb"]
---

This command sets the Y offset of the vehicle's center of mass when performing a wheelie. In order to perform a wheelie, the vehicle must be stopped or nearly stopped.

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieOffsetY( offset );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieOffsetY( offset )
```
{{ endtab }}
{{ endtabs }}

* **offset**: Sets the Y offset of the vehicle's center of mass when performing a wheelie. Positive numbers are up, negative are down.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieOffsetY(0.2);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieOffsetY(0.2)
```
{{ endtab }}
{{ endtabs }}

# Notes
See [SetWheelieOffsetX](/lucasmodlauncher/hacks/asf/con-commands/setwheelieoffsetx.md) and [SetWheelieOffsetZ](/hitandrun/scripting/con-commands/setwheelieoffsetz.md) to set offsets for the other two axes.