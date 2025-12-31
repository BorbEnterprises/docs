---
title: destroycars
description: "Fail the player if they destroy one or more cars."
summary:
    initialVersion: "1.18"
---

Fail the player if they destroy one or more cars.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("destroycars");
	// Optional: Specify specific car models the player will be penalised for. Defaults to all cars.
	AddCondTargetModel("glastruc");

	// Optional: Specify the total amount of cars they're allowed to destroy. Defaults to 1.
	SetCondTotal(2);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("destroycars")
	-- Optional: Specify specific car models the player will be penalised for. Defaults to all cars.
	Game.AddCondTargetModel("glastruc")

	-- Optional: Specify the total amount of cars they're allowed to destroy. Defaults to 1.
	Game.SetCondTotal(2)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this condition type.