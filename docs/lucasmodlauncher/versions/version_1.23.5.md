---
title: Version 1.23.5
description: "This update was released on September 7th, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on September 7th, 2019.**

# Launcher
## Mods List

* Made holding the Shift key when right clicking on one or more mods cause the `OutputPath` property in their `[Compile]` section(s) to be ignored.
    * This results in an ellipsis on the "Compile" button and also forces a browse dialog to ask you where to compile the mod(s) to.

## Launcher Settings

* Made it so settings that are not set to their default values are shown in bold.
* Made it so you can reset settings by right clicking them and clicking "Reset".
    * You can also right click on groups or the entire page (only the background, not the tab) to reset them as well.

# Mod Features

* Added support for minifying XML files when compiling mods. 
    * This defaults to enabled for non-decompilable mods.
    * Also added the `MinifyXMLs` property to the `[Compile]` section to opt in or out of this.

# Hacks
## Hack Support
Made crashes in the hack window procedure event save a crash dump before terminating the game.

## Additional Script Functionality
Added the `SetCollectibleSoundEffect` command to set the sound effect used when picking up a collectible in `delivery`, `dump` or `race` objectives. <!-- TODO: fact check the "race" objective -->

## Cheat Keys

* Made Shift+F4 to spawn a car not work when getting into a car.
* Made Shift+F4 to spawn a car not work during a forced car mission.
* Added `-forceallowcheatkeys` to opt out of the above two changes as well as a bunch of other safety checks including those added in Version 1.15.

## Console and Logging

* Added settings to include timestamps in the console and/or in log files.
* Added a setting to include categories (`[GAME]`, `[MOD]` or `[HACK]`) in the console and log files.

## Custom Traffic Support
Fixed a bug where parked car models didn't seem to get added if `AllocatedCars` was set to anything other than 5.

## Hover Car Refraction
Added a description to this hack.

## Resizable Window
Made it so crashes in the resizing timer callback save a crash dump before terminating the game.

## Sphere Maps
Added a description to this hack.