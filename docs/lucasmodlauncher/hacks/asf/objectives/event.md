---
title: event
description: "Pass the stage if the specified event is triggered."
summary:
    initialVersion: "1.18"
---

Pass the stage if the specified event is triggered.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
// Event 328 = State Prop Collectible Destroyed (like the nuclear waste in Level 7)
AddObjective("event", 328);
	// Specify the total amount of times the event must be triggered to pass the stage. Optional, defaults to 1.
	SetObjTotal(1);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Event 328 = State Prop Collectible Destroyed (like the nuclear waste in Level 7)
Game.AddObjective("event", 328)
	-- Specify the total amount of times the event must be triggered to pass the stage. Optional, defaults to 1.
	Game.SetObjTotal(1)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this objective type.