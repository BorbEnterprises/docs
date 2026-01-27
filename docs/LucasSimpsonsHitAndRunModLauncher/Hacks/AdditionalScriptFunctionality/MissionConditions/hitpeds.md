---
title: "hitpeds"
description: "Fail the player if they kick pedestrians."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
---

Fail the player if they kick pedestrians.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("hitpeds");
	// Optional: Specify specific characters. Defaults to all characters.
	AddCondTargetModel("marge");
	AddCondTargetModel("bart");

	// Optional: Specify the amount of times they're allowed to kick pedestrians. Defaults to 1.
	SetCondTotal(3);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("hitpeds")
	-- Optional: Specify specific characters. Defaults to all characters.
	Game.AddCondTargetModel("marge")
	Game.AddCondTargetModel("bart")

	-- Optional: Specify the amount of times they're allowed to kick pedestrians. Defaults to 1.
	Game.SetCondTotal(3)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
Hitting a pedestrian with your car does not count, only kicking them.