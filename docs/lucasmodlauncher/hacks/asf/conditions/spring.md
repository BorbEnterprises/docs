---
title: spring
description: "Fail the player if the bounce on a spring locator (typically used for air vents)."
summary:
    initialVersion: "1.18"
---

Fail the player if the bounce on a spring locator (typically used for air vents).

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("spring");
	// Optional: Specify the total amount of times the player is allowed to use springs. Defaults to 1.
	SetCondTotal(3);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("spring")
	-- Optional: Specify the total amount of times the player is allowed to use springs. Defaults to 1.
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