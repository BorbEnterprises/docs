---
title: "jump"
description: "Fail the player if they jump."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
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