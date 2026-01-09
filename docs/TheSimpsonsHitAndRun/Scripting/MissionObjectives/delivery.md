---
title: "delivery"
description: "This type of objective requires the player to collect items to pass the stage."
authors: [ 2, 735 ]
---

This type of objective requires the player to collect items to pass a stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("delivery");
	AddCollectible("m1_tomato", "scien");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("delivery")
	Game.AddCollectible("m1_tomato", "scien")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
You can add up to 32 collectibles per stage.