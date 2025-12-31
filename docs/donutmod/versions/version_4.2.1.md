---
title: Version 4.2.1
description: "This update was released on March 22nd, 2022."
---

**This update was released on March 22nd, 2022.**

# General

* Added `MaxTraffic = 0` to both level's `LV` tables.
* Changed the `AddNPCCharacterBonusMission` hook to only be installed when the Replayable Bonus Missions hack is enabled.
	* Previously, it was always installed and checked if the hack was enabled every time it was called which was **Mega Dumb:tm:**.

# Missions
## Level 2 Mission 7
Fixing a typo where instead of `MV.MaxTrafficLate` being set, `MV.MaxTrafficEarly` was being set again.

This change affects the amount of traffic cars during later stages of the mission.