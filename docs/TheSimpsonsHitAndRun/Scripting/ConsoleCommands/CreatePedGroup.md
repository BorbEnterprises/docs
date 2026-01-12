---
title: "CreatePedGroup"
description: "Creates a ped group that can be populated with subsequent calls to AddPed."
authors: [ 2 ]
---

This command creates a ped group that can be populated with subsequent calls to [[AddPed.md]].

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
CreatePedGroup( index );
```
{{ endtab }}
{{ tab Lua }}
```js
Game.CreatePedGroup( index )
```
{{ endtab }}
{{ endtabs }}

* **index**: The index of the ped group.

# Examples
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Examples/PedGroup.md }}

# Notes
By default, there are a maximum of 10 ped groups and the index can only be 0 through 9.

You can use the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomLimits.md]] hack to increase the maximum amount of ped groups.