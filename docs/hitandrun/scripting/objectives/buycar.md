---
title: buycar
description: "This type of objective requires the player to purchase or summon a specific vehicle to pass the stage."
authors: ["borb"]
---

This type of objective requires the player to purchase, summon, or enter a specific vehicle to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
This example demonstrates the way Radical uses these stages, preceded by a locked stage with the required vehicle specified.
```js
AddStage("locked","car","plowk_v");
	// Locked stages use INGAME_MESSAGE strings instead of MISSION_OBJECTIVE strings.
	// This would show INGAME_MESSAGE_00 after the objective is passed.
	SetStageMessageIndex(0);
	AddObjective("dialogue");
		...
	CloseObjective();
CloseStage();

AddStage();
	// The second argument to AddObjective() specifies the vehicle the player must have to pass the stage.
	// If the player starts the stage with this as their active vehicle, it will automatically pass.
	// Otherwise, they will have to purchase it or summon it from a phone booth.
	AddObjective("buycar", "plowk_v");
	CloseObjective();
CloseStage();
```
This example demonstrates a buycar objective being used without a locked stage before it. Despite Radical never using them in this manner, the objective still works as intended.
```js
AddStage();
	// The second argument to AddObjective() specifies the vehicle the player must have to pass the stage.
	// If the player starts the stage with this as their active vehicle, it will automatically pass.
	// Otherwise, they will have to purchase it or summon it from a phone booth.
	AddObjective("buycar", "plowk_v");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
This example demonstrates the way Radical uses these stages, preceded by a locked stage with the required vehicle specified.
```lua
AddStage("locked","car","plowk_v")
	-- Locked stages use INGAME_MESSAGE strings instead of MISSION_OBJECTIVE strings.
	-- This would show INGAME_MESSAGE_00 after the objective is passed.
	SetStageMessageIndex(0)
	AddObjective("dialogue")
		...
	CloseObjective()
CloseStage()

AddStage()
	-- The second argument to AddObjective() specifies the vehicle the player must have to pass the stage.
	-- If the player starts the stage with this as their active vehicle, it will automatically pass.
	-- Otherwise, they will have to purchase it or summon it from a phone booth.
	AddObjective("buycar", "plowk_v")
	CloseObjective()
CloseStage()
```
This example demonstrates a buycar objective being used without a locked stage before it. Despite Radical never using them in this manner, the objective still works as intended.
```lua
AddStage()
	-- The second argument to AddObjective() specifies the vehicle the player must have to pass the stage.
	-- If the player starts the stage with this as their active vehicle, it will automatically pass.
	-- Otherwise, they will have to purchase it or summon it from a phone booth.
	AddObjective("buycar", "plowk_v")
	CloseObjective()
CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.
