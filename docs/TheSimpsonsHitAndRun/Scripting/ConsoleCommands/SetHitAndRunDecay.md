---
title: "SetHitAndRunDecay"
description: "Sets the rate that the Hit & Run meter decreases when the player stops committing crimes."
authors: [ 2 ]
---

Sets the rate that the Hit & Run meter decreases when the player stops committing crimes.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunDecay( decay_rate );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunDecay( decay_rate )
```
{{ endtab }}
{{ endtabs }}

* **decay_rate**: The decay rate per second.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Example from Radical's scripts/missions/level01/leveli.mfk
SetHitAndRunDecay(3.0);
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Example from Radical's scripts/missions/level01/leveli.mfk
Game.SetHitAndRunDecay(3.0)
```
{{ endtab }}
{{ endtabs }}