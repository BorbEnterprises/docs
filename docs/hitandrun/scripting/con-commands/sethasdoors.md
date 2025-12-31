---
title: SetHasDoors
description: "Sets whether or not the player character opens the door upon entering a vehicle."
authors: ["borb"]
---

This command sets whether or not the player character opens the door upon entering a vehicle.

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetHasDoors( doors );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHasDoors( doors )
```
{{ endtab }}
{{ endtabs }}

* **doors**: Sets whether or not the player character opens the door upon entering a vehicle.
    * Defaults to 1.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetHasDoors(1);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHasDoors(1)
```
{{ endtab }}
{{ endtabs }}

# Notes
This command is overridden by [SetIrisTransition](setiristransition.md) in the event that both are present.
