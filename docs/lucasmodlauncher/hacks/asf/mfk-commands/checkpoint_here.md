---
title: CHECKPOINT_HERE
description: "Adds a checkpoint to a stage."
authors: ["loren"]
summary:
    initialVersion: "1.25"
---

This command adds a checkpoint to a stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
CHECKPOINT_HERE();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.CHECKPOINT_HERE()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	CHECKPOINT_HERE();

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.CHECKPOINT_HERE()

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes

* Where the player spawns, the ped group, the traffic group and more can be configured when a stage is resumed from a checkpoint with the following commands:
	* [SetCheckpointDynaloadData](setcheckpointdynaloaddata.md)
	* [SetCheckpointPedGroup](setcheckpointpedgroup.md)
	* [SetCheckpointResetPlayerInCar](setcheckpointresetplayerincar.md)
	* [SetCheckpointResetPlayerOutCar](setcheckpointresetplayeroutcar.md)
	* [SetCheckpointTrafficGroup](setcheckpointtrafficgroup.md)
	* Any parameters set with those commands also affect the defaults for subsequent checkpoints.
	* Furthermore, you can also use [IfCurrentCheckpoint](ifcurrentcheckpoint.md) to only execute certain commands when resuming from a checkpoint.
* What checkpoint is resumed from when failing or restarting is remembered by its index. So if you reached the second checkpoint, you will resume from the second checkpoint regardless of if its on the same stage.

# Version History
## 1.25
Added this command.