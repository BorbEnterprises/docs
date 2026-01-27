---
title: "collectwrench"
description: "Fail the player if they collect a wrench."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
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