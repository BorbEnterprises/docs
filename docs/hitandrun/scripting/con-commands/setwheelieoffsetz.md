---
title: SetWheelieOffsetZ
description: "Sets the Z offset of the vehicle's center of mass when performing a wheelie."
authors: ["borb"]
---

This command sets the Z offset of the vehicle's center of mass when performing a wheelie. In order to perform a wheelie, the vehicle must be stopped or nearly stopped.

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieOffsetZ( offset );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieOffsetZ( offset )
```
{{ endtab }}
{{ endtabs }}

* **offset**: Sets the Z offset of the vehicle's center of mass when performing a wheelie. Positive numbers are forward, negative are backward.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieOffsetZ(0.2);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieOffsetZ(0.2)
```
{{ endtab }}
{{ endtabs }}

# Notes
See [SetWheelieOffsetX](/lucasmodlauncher/hacks/asf/con-commands/setwheelieoffsetx.md) and [SetWheelieOffsetY](/hitandrun/scripting/con-commands/setwheelieoffsety.md) to set offsets for the other two axes.