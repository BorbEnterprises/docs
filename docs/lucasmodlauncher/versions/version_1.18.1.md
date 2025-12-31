---
title: Version 1.18.1
description: "This update was released on July 5th, 2018."
authors: ["loren","lucasc190"]
---

**This update was released on July 5th, 2018.**

# Launcher
## General
Made it so hacks in the "Hacks" folder whose versions do not match that of the Launcher get sent to the Recycle Bin instead of showing an error message.

## Mods List
Made the mods list remember which page it was on when exiting the Launcher and re-opening it.

# Hacks
## 3D Phone Booth Preview Support

* Fixed an issue when not using `DarkenLockedCars` where all cars in the phone booth would appear dark after closing and opening it.
* Fixed interference between the lights in the phone booth and the lights in the car shop.

## Additional Script Functionality

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

## Hack: Debug Test
### Miscellaneous Page

* Added "No Go To Objective Camera Focus" .
* Added "Allow Cancel Initial Walk".

## Hack: Debug Text
### "lights" page
Added this page.

## Hack: Force Mission Select Level Reload
Moved from the Settings page to the Developer page.