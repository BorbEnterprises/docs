---
title: "SetNumChaseCars"
description: "Sets the number of cars that will spawn during a Hit & Run."
authors: [ 2 ]
---

Sets the number of cars that will spawn during a Hit & Run.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetNumChaseCars( number_of_cars );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetNumChaseCars( number_of_cars )
```
{{ endtab }}
{{ endtabs }}

* **number_of_cars**: The number of chase cars to spawn.
	* Can be set anywhere from 0 to 5.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Example from Radical's scripts/missions/level01/leveli.mfk
SetNumChaseCars("1");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Example from Radical's scripts/missions/level01/leveli.mfk
Game.SetNumChaseCars(1)
```
{{ endtab }}
{{ endtabs }}