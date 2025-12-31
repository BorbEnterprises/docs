---
title: SetAllowSeatSlide
description: "Sets whether or not the player is allowed to slide into the driver's seat from the passenger's seat."
authors: ["borb"]
---

This command sets whether or not the player is allowed to slide into the driver's seat from the passenger's seat.

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetAllowSeatSlide( slide );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetAllowSeatSlide( slide )
```
{{ endtab }}
{{ endtabs }}

* **slide**: Sets whether or not the player can slide from the passenger's seat to the driver's seat.
    * Defaults to 1.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetAllowSeatSlide(1);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetAllowSeatSlide(1)
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.
