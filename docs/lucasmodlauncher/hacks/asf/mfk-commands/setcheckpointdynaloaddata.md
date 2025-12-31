---
title: SetCheckpointDynaLoadData
description: "Sets the dyna load data string to use when resuming a stage from a checkpoint."
authors: ["loren"]
summary:
    initialVersion: "1.25"
---

This command sets the dyna load data string to use when resuming a stage from a checkpoint.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

Additionally, this should be called alongside [CHECKPOINT_HERE](checkpoint_here.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCheckpointDynaLoadData( dyna_load_data );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCheckpointDynaLoadData( dyna_load_data )
```
{{ endtab }}
{{ endtabs }}

* **dyna_load_data**: The [dyna load data string](/hitandrun/misc/dyna-load-data.md) to execute.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	CHECKPOINT_HERE();
	SetCheckpointDynaLoadData("l1z1.p3d;l1r1.p3d;l1r7.p3d;");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.CHECKPOINT_HERE()
	Game.SetCheckpointDynaLoadData("l1z1.p3d;l1r1.p3d;l1r7.p3d;")

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