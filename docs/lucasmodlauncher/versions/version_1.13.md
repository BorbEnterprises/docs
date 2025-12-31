---
title: Version 1.13
description: "This update was released on January 7th, 2016."
authors: ["loren","lucasc190"]
---

**This update was released on January 7th, 2016.**

# Launcher
## Mods List

* Added "Show Newest File" to the right click menu of mods.
* Added the ability to compile mods that do not have an OutputPath property in their Compile section.
* Changed the copyright year of the Mod Launcher to 2016.
* Fixed a bug where an error message would appear after launching the game with the Mod Launcher's "-launch" command line argument.
* Fixed an issue that caused a crash when attempting to load non-UTF-8, non-ANSI Lua files.
* Improved crash dump saving.

## Mod Info

* Fixed a bug when combining authors with notes for the information box when multiple mods are selected.
* Made headers bold.
* Made the zoom level get saved.

## Mod Settings

* Made warnings only appear if the previous value didn't meet the warning condition.
* Unchanged mod settings are no longer stored.

# Mod Features

* Added the `Group` property to `[Author]` sections. This allows you to group authors together.
* Added the `Page` and `Group` properties to `[Setting]` sections. This allows you to organise your mod settings into pages and groups.
* Added the `UncompiledOnly` property to `[Setting]` sections. This will remove the setting when compiling the mod.
* Made `[SettingWarning]` sections work for all types of settings.
* Re-added for `MinifyArt` in the `[Compile]` section.

# Hacks
## Hack Support
Made the game support DPIs other than 96.

## Custom Dialogue Character Codes
Added support for Nongeneric Characters.

## Custom Files
{{ snippet lucasmodlauncher/versions/1.13/hack_custom-files }}

## Cheat Keys
Made keys only work once for each key press.

## Frame Limiter
Made this hack default to being ticked as the game has issues of varying severity at frame rates above or below a certain range (the game runs best at 60 FPS).