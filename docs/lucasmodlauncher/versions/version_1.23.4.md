---
title: Version 1.23.4
description: "This update was released on September 1st, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on September 1st, 2019.**

# Highlights
Two new mod hacks that reintroduce features from the console versions of the game:

* Hover Car Refraction
* Sphere Maps

# Launcher
## General

* Added a check for if you have Service Pack 3 installed when using Windows XP.
    * Also added the `-forcexpsp3check`, `-noxpsp3check` and `-spoofxpsp3check` command line arguments.
* Added the `-ignoreloaderrors` command line argument. This makes the Mod Launcher ignore errors when loading mods and hacks.

## Main Window
Fixed an issue where the update link still left a gap for the Account button when Donut Team Account Integration was disabled.

## Localisation
This version adds a couple new language strings related to the new Service Pack 3 check on Windows XP.

A new template language (Template_1.23.4.xml) was published on [this page](../localisation.md) including these new strings at the end of the file.

# Hacks
## Additional Script Functionality

* Fixed a crash when cancelling a mission or failing a mission and choosing "no" when the player is inside some types of disabled triggers.
* Made it so this hack does not assert if a locator is missing if Missing Locator Detection is enabled in Debug Checks.

## Bug Fixes
Made `FixZoneLoadOnExitCrash` also fix a crash when proceeding to another level from a mission that loads a zone when it ends (via `StreetRacePropsUnload`).

## Custom Limits
Added a `[Scripting]` section with a new `ArgumentLengthLimit` limit.

## Custom Vertex Shader Support
Added this new advanced hack.

## Debug Checks
Made the Missing Locator Detection show human readable text for locators that are missing for Additional Script Functionality commands.

## Debug Text
### "position" Page
Made this page show all action buttons the player is in with "(main)" after the main one (the one you can interact with) instead of just showing the main one.

## Hover Car Refraction
Added this new Setting mod hack. This reimplements the refraction effect for Professor Frink's Hover Car from the console versions of the game. This reimplementation is based on the Xbox version.

## Lens Flare
Removed an assert when failing to create the occlusion query when using `-testing`.

## Override Shader Parameters

* Added support for Vector parameters.
* Added support for the `ROTV`, `REFI`, `REFB` and `REFC` parameters.

## Refraction Shader Support
Added this new advanced hack. This reimplements the `refract` PDDI shader type from the console versions of the game.

## Sphere Maps
Added this new Setting mod hack. This improves reflections on cars by reimplementing the `spheremap` PDDI shader type from the console versions of the game. This reimplementation is based on the Xbox version.

By default, all `spheremap` shaders are remapped to be `environment` shaders on PC and this hack undoes that.