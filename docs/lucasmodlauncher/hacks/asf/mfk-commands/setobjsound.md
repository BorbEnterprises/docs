---
title: SetObjSound
description: "Set a sound to use for a hitpeds objective or the insidetrigger / outsidetrigger objectives."
summary:
    initialVersion: "1.18"
---

Set a sound to use for a [hitpeds objective](../objectives/hitpeds.md) or the [insidetrigger / outsidetrigger objectives](../objectives/insidetrigger-outsidetrigger.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
## hitpeds Objective
{{ tabs }}
{{ tab MFK }}
```js
SetObjSound( sound );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjSound( sound )
```
{{ endtab }}
{{ endtabs }}

* **sound**: The name of the daSoundResourceData to play.

## insidetrigger / outsidetrigger Objectives
{{ tabs }}
{{ tab MFK }}
```js
SetCondSound( sound, event, [time_between, start_delay] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondSound( sound, event, [time_between, start_delay] )
```
{{ endtab }}
{{ endtabs }}

* **sound**: The name of the daSoundResourceData to play.
* **event**: The event to play the sound on.
    * **enter_trigger**: Play the sound when entering the trigger.
    * **inside_trigger**: Play the sound when inside the trigger 
        * Only for "insidetrigger" objectives.
    * **outside_trigger**: Play the sound when outside the trigger 
        * Only for "outsidetrigger" objectives.
    * **exit_trigger**: Play the sound when exiting the trigger.
* **time_between**: The time between each time the sound plays in second 
    * Only for "inside_trigger" or "outside_trigger" events.
* **start_delay**: The delay before the sound starts playing after entering/exiting the trigger in seconds 
    * Only for "inside_trigger" or "outside_trigger" events.


# Examples
## hitpeds Objective
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("hitpeds");
	AddObjSound("generic_car_explode");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("hitpeds")
	Game.AddObjSound("generic_car_explode")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

## insidetrigger / outsidetrigger Objectives
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("insidetrigger");
	SetObjTrigger("z2phone1");

	SetObjSound("enter_trigger","gag_alm2");
	SetObjSound("inside_trigger","countdown_beeps",1,5);
	SetObjSound("exit_trigger","P_HitByC_Mrg_01");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("insidetrigger")
	Game.SetObjTrigger("z2phone1")

	Game.SetObjSound("enter_trigger","gag_alm2")
	Game.SetObjSound("inside_trigger","countdown_beeps",1,5)
	Game.SetObjSound("exit_trigger","P_HitByC_Mrg_01")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.