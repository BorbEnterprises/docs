---
title: "insidetrigger / outsidetrigger"
description: "Fail the player if they are inside or outside a trigger(s)."
authors: [ 2 ]
initialVersion:
	project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
	projectBranchVersion_id: 379 # 1.18
---

Fail the player if they are inside or outside a trigger(s).

# Examples
## insidetrigger
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("insidetrigger");
	// Required: Specify the locator whose triggers affect the condition.
	SetCondTrigger("z2phone1");
	
	// Optional: Specify the maximum amount of time the player is allowed to be in the triggers. Defaults to 0.
	SetCondThreshold(10);

	// Optional: Specify an objective message index to show when inside the trigger.
	SetCondMessageIndex(3);
	
	// Optional: Specify the decay rate of the meter when the player is not inside any of the triggers. Defaults to no decay.
	SetCondDecay(3, 2);
	
	// Optional: Specify a sound that will play when the player enters the trigger.
	SetCondSound("gag_alm2", "enter_trigger");
	
	// Optional: Specify a sound that will play when the player stays inside the trigger.
	//		You can only have an "inside_trigger" sound in an "insidetrigger" objective.
	SetCondSound("countdown_beeps", "inside_trigger", 1, 5);
	
	// Optional: Specify a sound that will play when the player exits the trigger.
	SetCondSound("P_HitByC_Mrg_01", "exit_trigger");
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("insidetrigger")
	-- Required: Specify the locator whose triggers affect the condition.
	Game.SetCondTrigger("z2phone1")
	
	-- Optional: Specify the maximum amount of time the player is allowed to be in the triggers. Defaults to 0.
	Game.SetCondThreshold(10)

	-- Optional: Specify an objective message index to show when inside the trigger.
	Game.SetCondMessageIndex(3)
	
	-- Optional: Specify the decay rate of the meter when the player is not inside any of the triggers. Defaults to no decay.
	Game.SetCondDecay(3, 2)
	
	-- Optional: Specify a sound that will play when the player enters the trigger.
	Game.SetCondSound("gag_alm2", "enter_trigger")
	
	-- Optional: Specify a sound that will play when the player stays inside the trigger.
	--		You can only have an "inside_trigger" sound in an "insidetrigger" objective.
	Game.SetCondSound("countdown_beeps", "inside_trigger", 1, 5)
	
	-- Optional: Specify a sound that will play when the player exits the trigger.
	Game.SetCondSound("P_HitByC_Mrg_01", "exit_trigger")
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

## outsidetrigger
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("outsidetrigger");
	// Required: Specify the locator whose triggers affect the condition.
	SetCondTrigger("z2phone1");

	// Optional: Specify a sound that will play when the player stays outside the trigger.
	//		You can only have an "outside_trigger" sound in an "outsidetrigger" objective.
	SetCondSound("countdown_beeps", "outside_trigger", 1, 5);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("outsidetrigger")
	-- Required: Specify the locator whose triggers affect the condition.
	Game.SetCondTrigger("z2phone1")

	-- Optional: Specify a sound that will play when the player stays outside the trigger.
	--		You can only have an "outside_trigger" sound in an "outsidetrigger" objective.
	Game.SetCondSound("countdown_beeps", "outside_trigger", 1, 5)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}