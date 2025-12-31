---
title: SetCheckpointResetPlayerOutCar
description: "Makes the player reset on foot when resuming a stage from a checkpoint."
authors: ["loren"]
summary:
    initialVersion: "1.25"
---

This command makes the player reset on foot when resuming a stage from a checkpoint.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

Additionally, this should be called alongside [CHECKPOINT_HERE](checkpoint_here.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCheckpointResetPlayerOutCar( player_locator, car_locator );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCheckpointResetPlayerOutCar( player_locator, car_locator )
```
{{ endtab }}
{{ endtabs }}

* **player_locator**: The name of a [Type 3 Locator](/pure3d/chunk-types/chunk-3000005.md#this_types_type3) that the player character will spawn on.
* **car_locator**: The name of a [Type 3 Locator](/pure3d/chunk-types/chunk-3000005.md#this_types_type3) that the player's car will spawn on.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	CHECKPOINT_HERE();
	SetCheckpointResetPlayerInCar("level1_homer_start", "level1_carstart");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.CHECKPOINT_HERE()
	Game.SetCheckpointResetPlayerInCar("level1_homer_start", "level1_carstart")

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