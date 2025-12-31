---
title: SetParkedCarsEnabled
description: "Set whether or not parked cars are enabled for the mission."
summary:
    initialVersion: "1.20"
---

Set whether or not parked cars are enabled for the mission.

# Context
{{ snippet hitandrun/command-contexts/mission-init-root }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetParkedCarsEnabled( parked_cars_enabled );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetParkedCarsEnabled( parked_cars_enabled )
```
{{ endtab }}
{{ endtabs }}

* **parked_cars_enabled**: Whether or not parked cars are enabled. 
    * Defaults to 1 (true) unless [StreetRacePropsLoad](/hitandrun/scripting/mfk-commands/streetracepropsload.md) is called in the mission.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");

	...

    StreetRacePropsLoad("l4_m1p.p3d;");
	StreetRacePropsUnload("l4_m1p.p3d:");
    
    // Enable parked cars even though Street Race Props are in use.
	SetParkedCarsEnabled(1);

	AddStage();
    	...
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")

	...

    Game.StreetRacePropsLoad("l4_m1p.p3d;")
	Game.StreetRacePropsUnload("l4_m1p.p3d:")
    
    -- Enable parked cars even though Street Race Props are in use.
	Game.SetParkedCarsEnabled(1)

	Game.AddStage()
    	...
	Game.CloseStage()
Game.CloseMission()

```
{{ endtab }}
{{ endtabs }}

# Notes
This command can be helpful for enabling parked cars in a mission where the "Street Race Props" would not interfere with the parked car locators (the original game's L1M7 could've used something like this).

# Version History
## 1.21
Removed the "!m_bStart" assert (previously on line [3336](/img/lucasmodlauncher/misc/asf_bStart_3336.png)) related to using this command.

## 1.20
Added this command.