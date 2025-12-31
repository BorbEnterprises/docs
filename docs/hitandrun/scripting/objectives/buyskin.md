---
title: buyskin
description: "This type of objective requires the player to purchase or wear a specific skin to pass the stage."
authors: ["borb"]
---

This type of objective requires the player to purchase or wear a specific skin to pass the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
This example demonstrates the way Radical uses these stages, preceded by a locked stage with the required skin specified.
```js
AddStage("locked","skin","l_cool");
	// Locked stages use INGAME_MESSAGE strings instead of MISSION_OBJECTIVE strings.
	// This would show INGAME_MESSAGE_03 after the objective is passed.
	SetStageMessageIndex(3);
	AddObjective("dialogue");
		...
	CloseObjective();
CloseStage();

AddStage();
	// The second argument to AddObjective() specifies the skin the player must have to pass the stage.
	// If the player starts the stage with this as their active skin, it will automatically pass.
	// Otherwise, they will have to purchase it or wear it at a skin shop.
	AddObjective("buyskin", "l_cool");
	CloseObjective();
CloseStage();
```
This example demonstrates a buyskin objective being used without a locked stage before it. Despite Radical never using them in this manner, the objective still works as intended.
```js
AddStage();
	// The second argument to AddObjective() specifies the skin the player must have to pass the stage.
	// If the player starts the stage with this as their active skin, it will automatically pass.
	// Otherwise, they will have to purchase it or wear it at a skin shop.
	AddObjective("buyskin", "l_cool");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
This example demonstrates the way Radical uses these stages, preceded by a locked stage with the required skin specified.
```lua
AddStage("locked","skin","l_cool")
	-- Locked stages use INGAME_MESSAGE strings instead of MISSION_OBJECTIVE strings.
	-- This would show INGAME_MESSAGE_03 after the objective is passed.
	SetStageMessageIndex(3)
	AddObjective("dialogue")
		...
	CloseObjective()
CloseStage()

AddStage()
	-- The second argument to AddObjective() specifies the skin the player must have to pass the stage.
	-- If the player starts the stage with this as their active skin, it will automatically pass.
	-- Otherwise, they will have to purchase it or wear it at a skin shop.
	AddObjective("buyskin", "l_cool")
	CloseObjective()
CloseStage()
```
This example demonstrates a buyskin objective being used without a locked stage before it. Despite Radical never using them in this manner, the objective still works as intended.
```lua
AddStage()
	-- The second argument to AddObjective() specifies the skin the player must have to pass the stage.
	-- If the player starts the stage with this as their active skin, it will automatically pass.
	-- Otherwise, they will have to purchase it or wear it at a skin shop.
	AddObjective("buyskin", "l_cool")
	CloseObjective()
CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.
