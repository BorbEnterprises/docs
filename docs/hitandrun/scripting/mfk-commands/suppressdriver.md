---
title: SuppressDriver
description: "Prevents a character from appearing in vehicles owned by the player (the default level car or those summoned from the phonebooth) in a level."
---

This command prevents a character from appearing in vehicles owned by the player (the default level car or those summoned from the phonebooth) in a level.

# Context
{{ snippet hitandrun/command-contexts/level-load }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SuppressDriver( character );
```
{{ endtab }}
{{ tab Lua }}
```js
Game.SuppressDriver( character )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character who will be unavailable as a driver in the level.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Used in Level 1 to prevent Homer appearing in his cars since he's the player character
SuppressDriver("homer");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Used in Level 1 to prevent Homer appearing in his cars since he's the player character
Game.SuppressDriver("homer")
```
{{ endtab }}
{{ endtabs }}

# Notes
There is a limit of 32 suppressed drivers in a level.