---
title: jump
description: "Fail the player if they jump."
summary:
    initialVersion: "1.18"
---

Fail the player if they jump.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("jump");
	// Optional: Specify the total amount of times the player is allowed to jump. Defaults to 1.
	SetCondTotal(3);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("jump")
	-- Optional: Specify the total amount of times the player is allowed to jump. Defaults to 1.
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