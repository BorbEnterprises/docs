---
title: collectcoins
description: "Fail the player if they collect coins."
summary:
    initialVersion: "1.18"
---

Fail the player if they collect coins.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("collectcoins");
	// Optional: Specify the amount of coins they're allowed to collect. Defaults to 1.
	SetCondTotal(3);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("collectcoins")
	-- Optional: Specify the amount of coins they're allowed to collect. Defaults to 1.
	Game.SetCondTotal(3)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this condition type.