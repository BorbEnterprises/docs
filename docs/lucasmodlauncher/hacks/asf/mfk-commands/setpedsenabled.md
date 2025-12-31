---
title: SetPedsEnabled
description: "Sets whether or not pedestrians are enabled for a mission."
summary:
    initialVersion: "1.20"
---

Sets whether or not pedestrians are enabled for a mission.

# Context
{{ snippet hitandrun/command-contexts/mission-init-root }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetPedsEnabled( peds_enabled );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetPedsEnabled( peds_enabled )
```
{{ endtab }}
{{ endtabs }}

* **peds_enabled**: Whether or not peds are enabled. 
    * Defaults to 1 (true) unless [StreetRacePropsLoad](/hitandrun/scripting/mfk-commands/streetracepropsload.md) is called in the mission.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");

	...

    StreetRacePropsLoad("l4_m1p.p3d;");
	StreetRacePropsUnload("l4_m1p.p3d:");
    
    // Enable Peds even though Street Race Props are in use.
	SetPedsEnabled(1);

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
    
    -- Enable Peds even though Street Race Props are in use.
	Game.SetPedsEnabled(1)

	Game.AddStage()
    	...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
This command can be helpful for enabling peds in a mission where the "Street Race Props" would not interfere with the ped paths (the original game's L1M7 could've used something like this).

# Version History
## 1.23.8
Fixed a bug where calling `SetPedsEnabled` alongside `StreetRacePropsLoad` would cause pedestrians to become disabled after the mission ends until another mission puts it back.

## 1.21
Removed the "!m_bStart" assert (previously on line [3292](/img/lucasmodlauncher/misc/asf_bStart_3292.png)) related to using this command.

## 1.20
Added this command.