---
title: Version 1.17
description: "This update was released on April 13th, 2018."
authors: ["loren","lucasc190"]
---

**This update was released on April 13th, 2018.**

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

# Hacks
## Hack Support
Made some debug asserts display more helpful error messages.

## Bug Fixes

* Added a new setting for applying depth to the Coin on the HUD.
* Changed this hack to be requirable and configurable by mods via BugFixes.ini.

## Custom Bonus Mission Support
Updated this hack with new functionality to this hack to prevent the game from resetting the player's position and forcing them into their car at the start of specific Street Race missions.

This is helpful if you're creating a mod that has an onfoot mission replacing one of the street races.

Here's an example CustomBonusMissionSupport.ini showcasing how to use this new functionality:

```ini
[L2SR3]
ResetPlayer=0
ForcePlayerInCar=0
```

NOTE: By default, the game's street race scripts also call commands that cause the player to get forced into their car at the start of the mission. This means that if you disable the game forcefully doing so on an unmodified street race, this will appear to do nothing. This is merely putting it in the script's hands, not making it so it can't be done.

## Custom Car Support
Car indices are now per mod and automagically remapped as necessary at runtime.

## Custom Character Support
Added this new hack. This hack allows you to enable the following booleans that are normally specific to Lisa and Marge (and their respective outfits) on any character:

* **IsLisa**: This boolean sets whether or not the game will adjust the Y position of the character upwards hen they're in a vehicle like how they do with Lisa.
* **IsMarge**: This boolean sets whether or not the game will adjust the positions of joints 33, 34 and 35 of the character's skeleton when they're in a vehicle (depending on the High Roof setting of the car).

## Custom Dialogue Character Codes

* Increased the limit of characters in the `[NongenericCharacters]` section from 128 to Infinite.
* Made indices in the `[NongenericCharacters]` section per mod and are automagically remapped as nessecary at runtime.
* Made the `[NongenericOutfits]` section support mapping an outfit by name.
    * This effectively deprecates the `[NongenericCharacters]` section.

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