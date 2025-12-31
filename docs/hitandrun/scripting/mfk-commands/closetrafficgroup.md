---
title: CloseTrafficGroup
description: "Closes a traffic."
authors: ["loren"]
---

This command closes a traffic group.

# Context
{{ snippet hitandrun/command-contexts/level-init }}

Additionally, this should only be called after a call to [CreateTrafficGroup](createtrafficgroup.md) and at least one call to [AddTrafficModel](addtrafficmodel.md).

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

# Notes
No additional notes.