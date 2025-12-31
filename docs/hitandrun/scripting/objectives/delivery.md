---
title: delivery
description: "This type of objective requires the player to collect items to pass the stage."
authors: ["legomariofanatic"]
---

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("delivery");
	AddCollectible( collectible_locator, composite_drawable_name );
	SetCollectibleEffect( collectible_effect );
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("delivery")
	Game.AddCollectible( collectible_locator, composite_drawable_name )
	Game.SetCollectibleEffect( collectible_effect )
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

* **collectible_locator**: The name of the Type 0 locator to place the collectible at.
* **composite_drawable_name** The name of the comppsite drawable to use for the collectible.
* * The `p3d` file containing this composite drawable must be loaded when starting the mission containing this objective type. Otherwise, the game will crash when reaching the stage containing this objective.
* **collectible_effect**: The name of the effect to use when collecting the collectible item.
* * Optional; defaults to `mission_col` if `SetCollectibleEffect()` is omitted.

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
* Up to 30 collectibles can be added inside this objective type. However, if more than 30 collectibles are added, the game will crash when reaching the stage containing this objective.
* `SetCollectibleEffect` can be used either once (in which case, the effect will be used for all collectibles preceeding `SetCollectibleEffect`) or for each collectible (in which case, the effect will be used for the single collectible preceeding `SetCollectibleEffect`).
