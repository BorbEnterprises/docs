---
title: SetCarChangeHitAndRunChange
description: "Set the amount the Hit & Run meter will change when swapping to a different vehicle."
summary:
    initialVersion: "1.18"
---

Set the amount the Hit & Run meter will change when swapping to a different vehicle.

# Context
{{ snippet hitandrun/command-contexts/level-init }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCarChangeHitAndRunChange( change_amount );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCarChangeHitAndRunChange( change_amount )
```
{{ endtab }}
{{ endtabs }}

* **change_amount**: The amount that will be added to the Hit & Run meter when changing your car. 
    * Defaults to -100.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetCarChangeHitAndRunChange(-100);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCarChangeHitAndRunChange(-100)
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.