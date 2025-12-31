---
title: SetWheelieOffsetX
description: "Sets the X offset of the vehicle's center of mass when performing a wheelie."
authors: ["borb"]
summary:
    initialVersion: "1.26"
---

This command sets the X offset of the vehicle's center of mass when performing a wheelie. In order to perform a wheelie, the vehicle must be stopped or nearly stopped.

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieOffsetX( offset );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieOffsetX( offset )
```
{{ endtab }}
{{ endtabs }}

* **offset**: Sets the X offset of the vehicle's center of mass when performing a wheelie. Positive numbers are right, negative are left.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetWheelieOffsetX(0.2);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWheelieOffsetX(0.2)
```
{{ endtab }}
{{ endtabs }}

# Notes
See [SetWheelieOffsetY](/hitandrun/scripting/con-commands/setwheelieoffsety.md) and [SetWheelieOffsetZ](/hitandrun/scripting/con-commands/setwheelieoffsetz.md) to set offsets for the other two axes.

# History
## 1.26
Added this command.