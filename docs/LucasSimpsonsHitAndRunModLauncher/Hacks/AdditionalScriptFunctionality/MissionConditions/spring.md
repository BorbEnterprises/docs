---
title: "spring"
description: "Fail the player if the bounce on a spring locator (typically used for air vents)."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
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