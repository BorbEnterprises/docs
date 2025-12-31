---
title: SetWeebleOffset
description: "Sets the Y offset of the vehicle's center of mass when in the air."
authors: ["borb"]
---

This command sets the Y offset of the vehicle's center of mass when in the air.

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetWeebleOffset( offset );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWeebleOffset( offset )
```
{{ endtab }}
{{ endtabs }}

* **offset**: Sets the Y offset of the vehicle's center of mass when in the air.
    * Defaults to -1.0.
	
# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetWeebleOffset(-0.85);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetWeebleOffset(-0.85)
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.
<span style="color:white">Fun Fact: Weebles wobble, but they don't fall down.</span>
