---
title: SetCheckpointPedGroup
description: "Sets the current ped group when resuming a stage from a checkpoint."
authors: ["loren"]
summary:
    initialVersion: "1.25"
---

This command sets the current ped group when resuming a stage from a checkpoint.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

Additionally, this should be called alongside [CHECKPOINT_HERE](checkpoint_here.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCheckpointPedGroup( ped_group );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCheckpointPedGroup( ped_group )
```
{{ endtab }}
{{ endtabs }}

* **ped_group**: The index of the ped group to use.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	CHECKPOINT_HERE();
	SetCheckpointPedGroup(7);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.CHECKPOINT_HERE()
	Game.SetCheckpointPedGroup(7)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.25
Added this command.