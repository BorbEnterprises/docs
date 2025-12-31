---
title: event
description: "Fail the player if the specified event is triggered."
summary:
    initialVersion: "1.18"
---

Fail the player if the specified event is triggered.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Event 328 = State Prop Collectible Destroyed (like the nuclear waste in Level 7)
AddCondition("event", 328);
	// Specify the total amount of times the event is allowed to be triggered before the player fails. Optional, defaults to 1.
	SetCondTotal(1);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Event 328 = State Prop Collectible Destroyed (like the nuclear waste in Level 7)
Game.AddCondition("event", 328)
	-- Specify the total amount of times the event is allowed to be triggered before the player fails. Optional, defaults to 1.
	Game.SetCondTotal(1)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this condition type.