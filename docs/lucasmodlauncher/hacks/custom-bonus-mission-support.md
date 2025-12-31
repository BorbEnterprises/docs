---
title: Custom Bonus Mission Support
description: "This hack allows mods to control various aspects of bonus missions such as the characters that host them."
---

**This hack must be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

This hack allows mods to control various aspects of bonus missions such as the characters that host them.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomBonusMissionSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomBonusMissionSupport.ini` and add the parameters necessary for your mod inside it.

```ini
; [Miscellaneous] Section
	; StreetRaceIntroDialogueMissionIndex: The dialogue index of the third street race character.
		; Defaults to 11. You probably won't have any reason to ever change this.
	
; [StreetRaceIntroDialogueMissionIndex] Section
	; CHARNAME: Bind a first or second street race character to index 9 or 10 respectively.
		; 9 is the index you would use for the SR1 NPC.
		; 10 is the index you would use for the SR2 NPC.
		; The SR3 NPC does not need to be assigned here.
	
; [StreetRaceIntroDialogueMissionIndexLX] Section
	; CHARNAME: Bind a first or second street race character to index 9 or 10 respectively.
		; 9 is the index you would use for the SR1 NPC.
		; 10 is the index you would use for the SR2 NPC.
		; The SR3 NPC does not need to be assigned here.
	
; [LXSRX] Section,
	; ResetPlayer: Force reset the mission once while initially loading it. 
		; Defaults to 1.
	; ForcePlayerInCar: Force the player in the car at the start of any given mission.
		; Defaults to 1.
	
; [LXMX] Section,
; [LXBM1] Section
	; These parameters can also be used on bonus missions and, contrary to the name of the hack, story missions.
	; The default values, however, are different.

	; ResetPlayer: Force reset the mission once while initially loading it.
		; Defaults to 0.
	; ForcePlayerInCar: Force the player in the car at the start of any given mission.
		; Defaults to 0.
	
[Miscellaneous]
StreetRaceIntroDialogueMissionIndex=11

[StreetRaceIntroDialogueMissionIndex]
; Level 1-6 SR1 and SR2 NPCs
milhouse=9
nelson=10

; Level 7 SR1 and SR2 NPCs
zmale3=9
zfem1=10

[L2SR3]
ResetPlayer=1
ForcePlayerInCar=1
```

# Version History
## 1.17
Updated this hack with new functionality to this hack to prevent the game from resetting the player's position and forcing them into their car at the start of specific Street Race missions.

## 1.15.1
Fixed a crash when launching the game with a non-cracked executable.

## 1.14
Added this hack.