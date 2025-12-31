---
title: Additional Script Functionality
sidebar_label: Introduction
description: "This hack adds several new mission objectives, mission conditions, script commands and other new script functionality."
---

**This is a [mod requirable hack](../all-hacks.md#mod-requirable-hacks) that must be required by a mod to be enabled.**

This hack adds several new mission objectives, mission conditions, script commands and other new script functionality.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=AdditionalScriptFunctionality
```

# Using This Hack
This hack simply provides additional commands you can use in MFK and CON scripts. You can find pages with more information listed below.

## CON Commands
See [All CON Commands](con-commands/all-commands.md).

## MFK Commands
See [All MFK Commands](mfk-commands/all-commands.md).

## Objective Types
See [All Objectives](objectives/all-objectives.md).

## Condition Types
See [All Conditions](conditions/all-conditions.md).

# Version History
## 1.26
{{ snippet lucasmodlauncher/versions/1.26/hack_additional-script-functionality }}

## 1.25.1
{{ snippet lucasmodlauncher/versions/1.25.1/hack_additional-script-functionality }}

## 1.25
{{ snippet lucasmodlauncher/versions/1.25/hack_additional-script-functionality }}

## 1.23.8

* Made it so this hack actually knows the previous or next stage when starting or ending a stage respectively.
	* In previous versions, the hack just guessed the previous or next stage by subtracting or adding one to the current stage index.
	* The old logic could cause issues in certain cases such as bombbarrel (nuclear waste) stages that can send you back multiple stages.
* Fixed a bug where calling `SetPedsEnabled` alongside `StreetRacePropsLoad` would cause pedestrians to become disabled after the mission ends until another mission puts it back.

## 1.23.5
Added the `SetCollectibleSoundEffect` command to set the sound effect used when picking up a collectible in `delivery`, `dump` or `race` objectives.

## 1.23.4
Made it so this hack does not assert if a locator is missing if Missing Locator Detection is enabled in Debug Checks.

## 1.23.1
Fixed a [conflict](/img/lucasmodlauncher/misc/asf_debugtest_conflict.png) between Additional Script Functionality and Debug Test when the "Menus > Pause Menu > Pause Always Allowed" setting was enabled in Debug Test.

## 1.22.4
Fixed an assert when starting a mission that has an "insidetrigger" or "outsidetrigger" objective or condition on its first stage.

## 1.22.3
Made triggers disabled with "DisableTrigger" in two or more subsequent stages stay disabled between the stages.

## 1.22
### General

* Fixed an issue introduced in 1.21 where there would be an assert when entering the bonus game.
* Made characters added to cars with ASF commands get removed from and re-added to the world when the car does instead of just when it explodes and is repaired.
    * Characters also now only get added immediately if the car is already in the world.
    * This resolves an issue where characters could remain floating in the air after the game removed a car.
* Made `g_CustomMissionData.empty()` only assert when using the `-testing` command line argument.

### MFK Commands

* Added `AddParkedCar`. This allows you to add a car to the level's parked cars list without needing it to be also added to a traffic group with AddTrafficModel.
* Added `UseTrafficGroup`. This sets the current traffic group index when getting to the mission via mission select or restarting it. This does not work unless the DynamicTraffic feature of CustomTrafficSupport is set to `Models` or `Slots`.

## 1.21
Removed "!m_bStart" asserts (previously on lines [3292](/img/lucasmodlauncher/misc/asf_bStart_3292.png) and [3336](/img/lucasmodlauncher/misc/asf_bStart_3336.png)) related to using the `SetPedsEnabled` and `SetParkedCarsEnabled` commands respectively.

## 1.20
### MFK Commands

* Added `SetParkedCarsEnabled`. This allows you to enable or disable parked cars for a mission.
* Added `SetPedsEnabled`. This allows you to enable or disable pedestrians for a mission.

## 1.19
### CON Commands

* Added the `AddVehicleCharacter` command.
* Added the `SetVehicleCharacterAnimation` command.
* Added the `SetVehicleCharacterJumpOut` command.
* Added the `SetVehicleCharacterScale` command.
* Added the `SetVehicleCharacterSuppressionCharacter` command.
* Added the `SetVehicleCharacterVisible` command.

### MFK Commands

* Added the `AddStageVehicleCharacter` command.
* Added the `RemoveStageVehicleCharacter` command.
* Added the `SetStageVehicleCharacterAnimation` command.
* Added the `SetStageVehicleCharacterJumpOut` command.
* Added the `SetStageVehicleCharacterScale` command.
* Added the `SetStageVehicleCharacterVisible` command.
* Added the `SetStageVehicleAllowSeatSlide` command.
* Updated `SetStageCharacterModel` to default the second argument to the player's current animation set instead of requiring the argument.

## 1.18.1
### New Features

* Added a new `none` display mode for `SetCondDisplay`. This mode is usable on all ASF conditions.
* Added a new `hitandrunlost` condition. This will fail the player if they lose the Hit & Run they have during the stage.
* Added a new `SetStageVehicleNoDestroyedJumpOut` command. This prevents a driver from jumping out of a car should it explode.
* Added a new `SetStageAllowMissionCancel` command. This prevents the player from restarting or cancelling the mission on the stage.
* Made ASF commands that take a boolean as an argument accept `true` or `false` as well as 0 or 1 instead of accepting any integer and treating it as true if it's not 0.

### Bug Fixes

* Fixed an issue where calling `SetStageCharacterModel` on a stage that calls `RESET_TO_HERE` that is preceded by another stage that calls `SetStageCharacterModel` (with the same model and animation set) didn't work.
* Fixed an issue where pressing enter to continue after restarting from a failed delayed condition in a reset-in-car mission with "Action/Get Out" bound to enter would cause you to exit your vehicle after the mission restarted.
* Fixed an issue where `hitandrunlost` stages that also call `SetStageHitAndRun(100);` to trigger a hit and run would automatically complete if you entered the stage without already having a Hit & Run.

## 1.18
Added this hack.