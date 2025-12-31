---
title: collectwrench
description: "Fail the player if they collect a wrench."
summary:
    initialVersion: "1.18"
---

Fail the player if they collect a wrench.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("collectwrench");
	// Optional: Specify the amount of wrenches they're allowed to collect. Defaults to 1.
	SetCondTotal(2);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("collectwrench")
	-- Optional: Specify the amount of wrenches they're allowed to collect. Defaults to 1.
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