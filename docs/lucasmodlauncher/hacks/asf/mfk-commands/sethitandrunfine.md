---
title: SetHitAndRunFine
description: "Set the amount of coins the player will be fined if they are caught in a Hit & Run."
summary:
    initialVersion: "1.18"
---

Set the amount of coins the player will be fined if they are caught in a Hit & Run.

# Context
{{ snippet hitandrun/command-contexts/level-init }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunFine( fine_amount );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunFine( fine_amount )
```
{{ endtab }}
{{ endtabs }}

* **fine_amount**: The amount to fine the player if they get caught. 
    * Defaults to 50.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunFine(50);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunFine(50)
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.