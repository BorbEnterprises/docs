---
title: "CreateTrafficGroup"
description: "Creates a traffic group that can be populated with subsequent calls to AddTrafficModel."
authors: [ 2 ]
---

This command creates a traffic group that can be populated with subsequent calls to [[AddTrafficModel.md]].

# Context
{{ Snippet:TheSimpsonsHitAndRun/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
CreateTrafficGroup( index );
```
{{ endtab }}
{{ tab Lua }}
```js
Game.CreateTrafficGroup( index )
```
{{ endtab }}
{{ endtabs }}

* **index**: The index of the traffic group.

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

# Notes
By default, the game only supports a single traffic group with an index of 0. 

You use the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomTrafficSupport.md]] hack to create more than one.