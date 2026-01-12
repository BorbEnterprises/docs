---
title: "CloseTrafficGroup"
description: "Closes a traffic group."
authors: [ 2 ]
---

This command closes a traffic group.

# Context
{{ Snippet:TheSimpsonsHitAndRun/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
CloseTrafficGroup();
```
{{ endtab }}
{{ tab Lua }}
```js
Game.CloseTrafficGroup()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
CreateTrafficGroup(0);
	AddTrafficModel("pizza", 5);
CloseTrafficGroup();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.CreateTrafficGroup(0)
	Game.AddTrafficModel("pizza", 5)
Game.CloseTrafficGroup()
```
{{ endtab }}
{{ endtabs }}