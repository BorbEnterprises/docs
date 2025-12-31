---
title: ClosePedGroup
description: "Closes a ped group."
authors: ["loren"]
---

This command closes a ped group.

# Context
{{ snippet hitandrun/command-contexts/level-init }}

Additionally, this should only be called after a call to [CreatePedGroup](createpedgroup.md) and at least one call to [AddPed](addped.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
ClosePedGroup();
```
{{ endtab }}
{{ tab Lua }}
```js
Game.ClosePedGroup()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ snippet hitandrun/mfk-commands/ped-group-example }}

# Notes
No additional notes.