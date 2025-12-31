---
title: SetHitAndRunDecayHitAndRun
description: "Set the amount the Hit & Run meter will decay each second while the player is in a Hit & Run."
summary:
    initialVersion: "1.18"
---

Set the amount the Hit & Run meter will decay each second while the player is in a Hit & Run.

# Context
{{ snippet hitandrun/command-contexts/level-init }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunDecayHitAndRun( decay_rate );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunDecayHitAndRun( decay_rate )
```
{{ endtab }}
{{ endtabs }}

* **decay_rate**: The rate at which the meter will decay while in a Hit & Run. 
    * Defaults to 6.0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunDecayHitAndRun(6.0);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunDecayHitAndRun(6.0)
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.