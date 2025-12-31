---
title: Version 1.20
description: "This update was released on December 22nd, 2018."
authors: ["loren","lucasc190"]
---

**This update was released on December 22nd, 2018.**

# Highlights

* New Custom Trigger Actions hack for binding custom actions to triggers.
* New mission commands in ASF for toggling pedestrians and parked cars for missions.
* Several new setting hacks including a fancy Letterbox hack.

# Launcher
## General

* Added the `-nocommandlinefile` command line argument.
* Added the `-nodeleteold` command line argument.
* Added the `-ignorelaunchmodconflicts` command line argument.
* Added the `-nowatermark` command line argument.
* Fixed an issue where ampersands were incorrectly escaped for the tray icon hover text.
* Made launching the game detect types of conflicts that previously were only detected when ticking mods.
* Made the `-allowignoremodconflicts` command line argument also allow the user to ignore conflicts detected when launching the game.

## Main Window

* Made "Close Launcher" default to being unticked (based on the results of [this poll](https://www.strawpoll.me/16597320/r)).

## Localization
This version introduces a new language string for when a conflict is detected upon launching the game.

A new template language (Template_1.20.xml) was published on [this page](../localisation.md) including this new language string at the end of the file.

# Hacks
## Additional Script Functionality
This update introduces a couple new script commands for missions.

* Added `SetParkedCarsEnabled`. This allows you to enable or disable parked cars for a mission.
* Added `SetPedsEnabled`. This allows you to enable or disable pedestrians for a mission.

## Aspect Ratio Support
Added the "Movie Letterbox Colour" setting.

## Custom Trigger Actions
Added this new hack. This allows you to bind various custom actions to specific triggers or events with optional conditions.


## Debug Test
### General
Renamed the "Sky" page to "World Spheres".

### Menus Page
Removed "No Camera Animations" in the "Main Menu" section.

### World Spheres Page
Added "Activate Dynamic World Spheres" as a setting instead of forcing it when this hack was enabled.

### Miscellaneous Page

* Removed "Allow Cancel Initial Walk".
* Removed "No Go To Objective Camera Focus".

## Debug Text
### General
Added a "world spheres" Page that shows information about any currently loaded World Spheres and their respective Lens Flares (if applicable).

### "cars" Page
Added "Parked cars enabled" to show if parked cars are currently enabled.

### "paths" Page

* Added "Enabled" to show if pedestrians are currently enabled.
* Added "Group" to show the currently selected ped group.
* Added information about all the ped groups that exist.

## Lens Flare

* Made Lens Flares not get enqueued if their World Sphere is deactivated.
    * Also added the `-deactivatedworldspherelensflares` command line argument to suppress this behaviour.
    * This fixes an issue where deactivating a world sphere would not deactivate its lens flare.

## Other Hacks
This version introduces several new Setting hacks.

* Cancellable Initial Walk
    * Allows you to interrupt the character walking at the start of a level.
* Letterbox
    * Allows you to force the game into a specific aspect ratio regardless of the game window's dimensions.
    * This may prove helpful for speedrunners who want to maximize their game window or play in full screen while forcing the game into 4:3.
* No Go To Objective Camera Focus
    * Disables the game taking control of the camera when you step near the target on foot in a "goto" stage.
* No Main Menu Camera Animations
    * Disables the camera animations on the main menu.
    * This hack is requirable as well if a mod calls for it.
* No Wrenches
    * Fully disables wrenches.
* One Tap Player Car Death
    * Makes the player's car get destroyed in one hit.
    * This hack has various options for what types of thing annihilate the player's car.