---
title: Version 22
description: "This update was released on March 7th, 2019."
---

**This update was released on March 7th, 2019.**

# Launcher
## General

* Now based on [Lucas' Simpsons Hit & Run Mod Launcher 1.22](../../lucasmodlauncher/versions/version_1.22.md).
* Fixed a silent crash on exit.
* Made default mods that conflict with enabled mods get ignored.
* Now supports many of the main Mod Launcher's command line arguments.
    * Also added support for "CommandLine.txt".
    * Also added `-multiplayersupersprint`. This allows you to go into the Bonus Game but doesn't do anything to make that support SHAR MP.
    * Also added `-noignoreenabledmods`.
    * Also added `-ignoredefaultallowedmods`.
    * Also added `-ignoredefaultenabledmods`.
    * Also added `-noignoreconflictingdefaultmods`.
    * Also added `-ignoredefaultmod`.
    * Also added `-modlaunchermods`.

# Settings

* Added a Mirror Mode mutator that enables the new Mirror Mode hack.
* Added a No Cheats mutator that enables the No Cheats hack and disables all other check hacks.
* Made the window only close after the game has been successfully launched.
* Made this window use the icon of the current configuration.
    * Only if using one other than "Main".
    * This can be disabled with the `-notitleconfiguration` command line argument.
* Replaced the "Token" field with an "Account..." button.
    * Also added a `-nomultiplayeraccountbutton` command line argument to revert this.

# Mods
Made the 3D Phone Booth Previews, No License Screen Delay and No HUD mods allowed by default.

# Hacks
## Multiplayer
Increased the following limits using [Custom Limits](../../lucasmodlauncher/hacks/custom-limits.md):

* Set the `[Miscellaneous]` `CarLimit` to 64.
* Set the `[Miscellaneous]` `ActionButtonLimit` to 184.
* Changed the `[Billboards]` `QuadLimit` limit from 600 to 1300.
* Set the `[CollisionIndices]` `VehicleLimit` to 64.
* Set the `[CollisionIndices]` `CharacterLimit` to 64.
* Set the `[CollisionIndices]` `DynaPhysLimit` to 115.