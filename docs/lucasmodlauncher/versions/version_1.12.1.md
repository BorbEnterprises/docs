---
title: Version 1.12.1
description: "This update was released on November 7th, 2015."
authors: ["loren","lucasc190"]
---

**This update was released on November 7th, 2015.**

# Launcher
## General
Fixed a bug where if "Close Launcher" was ticked and the Console window was closed while hack support was still initialising, the mod launcher would close.

## Main Window
Fixed a bug where the main window would remain disabled if the game was terminated while showing a window modal to the main window.

## Mods List
Made it so the "Compile" right click menu item will no longer show up in a category that doesn't support compilable mods.

## Launcher Settings

* made it so the "Advanced" tab has a scrollbar if you resize the window small enough.
* Made it so the "Licenses" tab only shows licenses for the hacks that are currently loaded.
    * Meaning if you remove every hack that used a particular license from the Hacks folder, the license will no longer appear here.

# Mod Features
Removed the `MinifyArt` and `MinifyScripts` properties of the `[Compile]` section because they were broken.

# Hacks
## Custom Files
### Lua Scripting
Fixed a bug where using `GetSetting` on an `Integer` type `Number` setting would return a number.

## Flippable Cars
Added a setting for whether or not Chase cars can flip over since the game does not reset these cars. This is disabled by default.