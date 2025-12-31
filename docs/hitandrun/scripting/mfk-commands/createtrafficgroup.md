---
title: CreateTrafficGroup
description: "Creates a traffic group that can be populated with subsequent calls to AddTrafficModel."
authors: ["loren"]
---

This command creates a traffic group that can be populated with subsequent calls to [AddTrafficModel](addtrafficmodel.md).

# Context
{{ snippet hitandrun/command-contexts/level-init }}

Additionally, this should be followed by at least one call to [AddTrafficModel](addtrafficmodel.md) and a call to [CloseTrafficGroup](closetrafficgroup.md).

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

Mods can use the [Mod Launcher's](/lucasmodlauncher/intro.md) [Custom Traffic Support](/lucasmodlauncher/hacks/custom-traffic-support.md) hack to create more than one.