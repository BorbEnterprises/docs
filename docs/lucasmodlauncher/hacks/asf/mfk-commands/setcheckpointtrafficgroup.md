---
title: SetCheckpointTrafficGroup
description: "Sets the current traffic group when resuming a stage from a checkpoint."
authors: ["loren"]
summary:
    initialVersion: "1.25"
---

This command sets the current traffic group when resuming a stage from a checkpoint.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

Additionally, this should be called alongside [CHECKPOINT_HERE](checkpoint_here.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCheckpointTrafficGroup( traffic_group );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCheckpointTrafficGroup( traffic_group )
```
{{ endtab }}
{{ endtabs }}

* **traffic_group**: The index of the traffic group to use.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	CHECKPOINT_HERE();
	SetCheckpointTrafficGroup(7);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.CHECKPOINT_HERE()
	Game.SetCheckpointTrafficGroup(7)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ snippet lucasmodlauncher/notes/dynamic-traffic-required }}

# Version History
## 1.25
Added this command.