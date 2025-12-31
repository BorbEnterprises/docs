---
title: SetStagePayout
description: "Set an amount of coins to give the player when they complete the stage."
summary:
    initialVersion: "1.18"
---

Set an amount of coins to give the player when they complete the stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStagePayout( coins );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStagePayout( coins ) 
```
{{ endtab }}
{{ endtabs }}

* **coins**: The amount of coins to give the player upon completing the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// Free 25 coins when you finish this stage.
	SetStagePayout(25);
		
	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	-- Free 25 coins when you finish this stage.
	Game.SetStagePayout(25)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.