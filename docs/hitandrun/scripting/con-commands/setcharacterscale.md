---
title: SetCharacterScale
description: "Sets the scale of the driver and the passenger in a vehicle."
authors: ["loren"]
---

This command sets the scale of the driver and the passenger in a vehicle.

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCharacterScale( scale );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCharacterScale( scale )
```
{{ endtab }}
{{ endtabs }}

* **scale**: The scale of the characters.
    * Defaults to 1.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetCharacterScale(1);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCharacterScale(1)
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.