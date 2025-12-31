---
title: hitpeds
description: "Fail the player if they kick pedestrians."
summary:
    initialVersion: "1.18"
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
This type of objective is not advanced by hitting pedestrians with a car.

# Version History
## 1.18
Added this condition type.