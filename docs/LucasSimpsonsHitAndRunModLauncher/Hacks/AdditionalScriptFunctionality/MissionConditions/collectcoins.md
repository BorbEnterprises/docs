---
title: "collectcoins"
description: "Fail the player if they collect coins."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
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