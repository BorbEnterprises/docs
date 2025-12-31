---
title: hitandrun
description: "Fail the player if they get a Hit & Run."
summary:
    initialVersion: "1.18"
---

Fail the player if they get a Hit & Run.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("hitandrun");
	// Optional: Specify a delay for the mission failed screen. Defaults to 2 seconds.
	//	  This is to allow enough time for the Hit & Run text to 
	//	  disappear before showing the mission failed screen.
	SetCondDelay(2);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("hitandrun")
	-- Optional: Specify a delay for the mission failed screen. Defaults to 2 seconds.
	--	  This is to allow enough time for the Hit & Run text to 
	--	  disappear before showing the mission failed screen.
	Game.SetCondDelay(2)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this condition type.