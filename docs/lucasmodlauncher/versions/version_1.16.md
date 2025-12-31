---
title: Version 1.16
description: "This update was released on September 15th, 2017."
authors: ["loren","lucasc190"]
---

**This update was released on September 15th, 2017.**

# Launcher
## General

* Added a "Game Install" button to the "Open..." menu on the bottom left of the main window.
* Made the Mod Launcher warn you if the Simpsons executable you select is not in a game folder.

# Mod Features

* Added a `Credits` boolean to `[Author]` sections to show them on the new "Credits" section to the Mod Information panel.
* Made it so an `[Author]` section can have multiple `Group` properties defined.
* Made it so you can specify `AuthorGroup` propeties in the `[Miscellaneous]` section of a Mod's `Meta.ini` to control the order of the groups.

# Hacks
## Hack Support
Made it take the game out of fullscreen when showing message windows.

## Aspect Ratio Support
Made the translucent black polygon in the background of the phonebooth handle different aspect ratios better.

## Custom Limits
Fixed a bug where CustomLimits.ini was not included when compiling mods.

## Custom Road Behaviour
Added this new hack. This allows you to define custom behaviour for specific roads.

## Custom Stats Totals
Made the "Clothes" and "Vehicles" menus get disabled in the scrapbook if there aren't any clothes or vehicles registered respectively.

## Multiplayer
Fixed a bug where Multiplayer.xml was not included when compiling mods.

## No Cheats
Made this hack tickable but hidden by default.

## No Fast Car Reset
Made it requirable by mods and hacks.

## No Inactive Dynamic Object Collisions
Added this new hack. This affects the behaviour of physics props.

## No Mission Start Cameras
Added this new hack. This is a Setting hack that disables mission start cameras.

## Resizable Window
Added this new hack. This allows you to resize the game window.

## Road Names
Added this new advanced hack. This keeps track of road names for other hacks to use.

## Screenshots

* Made it play a sound when taking a screenshot.
    * Customisable by mods.
* Made it flash the screen when taking a screenshot.
* Made Control+F12 take a screenshot that excludes the HUD.
