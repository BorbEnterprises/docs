---
title: AddPed
description: "Adds a ped to a ped group."
authors: ["loren"]

# TODO: Fact check the Notes section with Lucas.

---

This command adds a ped to a ped group.

# Context
{{ snippet hitandrun/command-contexts/level-init }}

Additionally, it must be called between calls to [CreatePedGroup](createpedgroup.md) and [ClosePedGroup](closepedgroup.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddPed( character, amount );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddPed( character, amount )
```
{{ endtab }}
{{ endtabs }}

* **character**: The name of the character to add to the ped group.
* **amount**: The maximum amount of this character that will be able to spawn.
	* Max of 7.

# Examples
{{ snippet hitandrun/mfk-commands/ped-group-example }}

# Notes
The total `amount` values of every call to this command within a ped group should not exceed 7.