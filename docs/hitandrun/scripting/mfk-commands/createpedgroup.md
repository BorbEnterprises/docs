---
title: CreatePedGroup
description: "Creates a ped group that can be populated with subsequent calls to AddPed."
authors: ["loren"]
---

This command creates a ped group that can be populated with subsequent calls to [AddPed](addped.md).

# Context
{{ snippet hitandrun/command-contexts/level-init }}

Additionally, this should be followed by at least one call to [AddPed](addped.md) and a call to [ClosePedGroup](closepedgroup.md).

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
{{ snippet hitandrun/mfk-commands/ped-group-example }}

# Notes
By default, there are a maximum of 10 ped groups and the index can only be 0 through 9.

As of Version 1.25, the [Mod Launcher's](/lucasmodlauncher/intro.md) [Custom Limits](/lucasmodlauncher/hacks/custom-limits.md) hack can be used to increase the maximum amount of ped groups.