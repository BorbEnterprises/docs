---
title: AddStage
description: "Adds a stage in a mission."
authors: ["loren"]
---

This command adds a stage to a mission.

# Context
{{ snippet hitandrun/command-contexts/mission-init-root }}

Additionally, this command should be followed by an objective and a call to [CloseStage](closestage.md).

# Syntax
## Regular Stage
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage();
```
{{ endtab }}
{{ endtabs }}

## Final Stage
{{ tabs }}
{{ tab MFK }}
```js
AddStage("final");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage("final");
```
{{ endtab }}
{{ endtabs }}

Giving this command "final" as its first argument marks a stage as being the final stage of the mission.

This indicates to the game that it should show "Mission Complete!" on the screen when the mission ends and, for most missions, marks it as complete in your save data.

There should be no subsequent stages after such a stage.

## Locked Stage
{{ tabs }}
{{ tab MFK }}
```js
AddStage("locked", type, name);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage("locked", type, name)
```
{{ endtab }}
{{ endtabs }}

Giving this command "locked" as its first argument allows you to show a prompt the stage ends if the player's current car or skin does not match the one specified by the following parameters:

* **type**: Set to "car" or "skin" depending on what you'd like to check for in the mission.
* **name**: The name of a car or skin that the player must have to avoid the prompt.

These types of stages typically use [dialogue objectives](../objectives/dialogue.md) so the prompt is shown after an NPC explains why you need a specific car or skin but this is **not** a requirement.

The message shown in this prompt is determined by [SetStageMessageIndex](setstagemessageindex.md).

These types of stages are also typically coupled with a [buycar objective](../objectives/buycar.md) or a [buyskin objective](../objectives/buyskin.md) that require the player to buy the given car or skin on the next stage but this is also **not** a requirement.

Regardless, you must have at least one subsequent stage of *any* type following a locked stage for its message to appear.

# Examples
## Regular Stage
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1sd");
	...

	// Simple timer stage as the final stage in a Sunday Drive mission
	// Do not use final in these missions!
	AddStage();
		AddObjective("timer");
			SetDurationTime(1);
		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1sd")
	...

	-- Simple timer stage as the final stage in a Sunday Drive mission
	-- Do not use final in these missions!
	Game.AddStage()
		Game.AddObjective("timer")
			Game.SetDurationTime(1)
		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

## Final Stage
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	...

	// Simple timer stage as the final stage in a story mission
	// Will show "Mission Complete!" when it ends
	AddStage();
		AddObjective("timer");
			SetDurationTime(1);
		CloseObjective();
	CloseStage();

	// Do not have stages after a final stage!

CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")
	...

	-- Simple timer stage as the final stage in a story mission
	-- Will show "Mission Complete!" when it ends
	Game.AddStage("final")
		Game.AddObjective("timer")
			Game.SetDurationTime(1)
		Game.CloseObjective()
	Game.CloseStage()

	-- Do not have stages after a final stage!

Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

## Locked Stage
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m3sd");
	...

	AddStage("locked","car","plowk_v");
		// Show INGAME_MESSAGE_00 in GenericPrompt.pag in ingame.p3d
		// After the dialogue if the player does not have the Plow King (plowk_v).
		SetStageMessageIndex(0);

		AddObjective("dialogue");
			...
		CloseObjective();
	CloseStage();

	// As mentioned above, this specific type of objective (buycar) is NOT required
	// in the subsequent stage but a subsequent stage in general IS required.
	AddStage(0);
		SetHUDIcon("barne");
		SetStageMessageIndex(239);

		AddObjective("buycar", "plowk_v");
		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m3sd")
	...

	Game.AddStage("locked","car","plowk_v")
		-- Show INGAME_MESSAGE_00 in GenericPrompt.pag in ingame.p3d
		-- After the dialogue if the player does not have the Plow King (plowk_v).
		Game.SetStageMessageIndex(0)

		Game.AddObjective("dialogue")
			...
		Game.CloseObjective()
	Game.CloseStage()

	-- As mentioned above, this specific type of objective (buycar) is NOT required
	-- in the subsequent stage but a subsequent stage in general IS required.
	Game.AddStage(0)
		Game.SetHUDIcon("barne")
		Game.SetStageMessageIndex(239)

		Game.AddObjective("buycar", "plowk_v")
		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
Radical often gives numbers as arguments to this command in many of their scripts. These are meaningless and do nothing.