---
title: "Version 1.17"
description: "Changelog for Version 1.17 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on April 13, 2018.**

# Launcher
## General
* Added a loading window on startup and when reloading mods using the Reload button.
* Added the `-noscanmodfiles` command line argument. This can be used to speed up the loading of mod files but disables the following functionality:
    * Conflict detection between non-compiled mods.
    * Showing the file size of mods.
    * Showing the newest file in non-compiled mods.
    * Showing the correct modified date on non-compiled mods.
* Fixed an issue where the title of message boxes on Windows XP were incorrectly set to "Error" rather than the name of the launcher.

## Account Integration
A number of changes were made to the way the Mod Launcher communicates with the Donut Team website. This corrects the recent issue where Play History was not working.

# New Hacks
## Custom Character Support
Added this new hack. This hack allows you to enable the following booleans that are normally specific to Lisa and Marge (and their respective outfits) on any character:

* **IsLisa**: This boolean sets whether or not the game will adjust the Y position of the character upwards hen they're in a vehicle like how they do with Lisa.
* **IsMarge**: This boolean sets whether or not the game will adjust the positions of joints 33, 34 and 35 of the character's skeleton when they're in a vehicle (depending on the High Roof setting of the car).

## Custom Interior Support
Added this new hack. This hack can be used to add new interior definitions or remove existing ones.

## Custom Save Data
Added this new advanced hack. This allows other hacks to store custom save data inside save files.

## Debug Checks
Added this new hack. Enabled and hidden by default.

This hack adds a number of checks to inform you of things such as possible corruption and missing locators (this functionality is experimental).

## Debug Hashes.
Added this new hack.

## Debug Test
Added this new hack. Hidden by default.

This hack contains a wide variety of half of unfinished or experimental features. It is now being included in the public release so  anyone can freely try these features out. 

**NOTE:** Functionality of this hack may be removed or altered without warning in future updates of the Mod Launcher. This hack SHOULD NOT be used when playtesting mods you are creating as some of it's features may cause the game to crash or behave in unexpected ways.

## Debug Text
Added this new hack. This hack makes a wide variety of different debug information display ingame. These pages can be cycled through with the T and R keys.

## Increased Reward Limits
Added this new hack. This hack increases some reward related limits.

# Updated Hacks
## Hack Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17/Hacks/HackSupport.md }}

## Bug Fixes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17/Hacks/BugFixes.md }}

## Custom Bonus Mission Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17/Hacks/CustomBonusMissionSupport.md }}

## Custom Car Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17/Hacks/CustomCarSupport.md }}

## Custom Dialogue Character Codes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.17/Hacks/CustomDialogueCharacterCodes.md }}