---
title: "Version 1.19"
description: "Changelog for Version 1.19 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on October 2, 2018.**

# Banner
![Version 1.19 Release Banner](/img/LucasSimpsonsHitAndRunModLauncher/VersionBanners/1.19.png)

# Highlights
* **Additional Script Functionality**: Vehicle Character Commands
* Language Localization Support for the Mod Launcher's Interface
    * The Mod Launcher still only ships with English.
* Lens Flare Hack
* Video Texture Support Hack

# Launcher
## General
* Added **dbghelp.dll** to the DLLs folder. This is used to save crash dumps.
* Added the `-debugloadhacks` command line argument.
* Added the `-loadhackspause` command line argument.
* Fixed a crash when using `-launch` with **Start in Correct Resolution** enabled (as is the default).
* Made the game only start in the correct width and height when starting windowed.
* Made the Mod Launcher restart if the shift key is held down when reloading all mods.
* Made the unhandled exception message have an error icon instead of no icon.
* Removed limitations on how many mods, hacks and mod settings could be injected into the game.
	* You don't want to know.

## Main Window
* Made the main window re-centre to the screen the loading window was moved to if it was moved to another screen while reloading.
* Made the main window start on the screen the loading window was last on.
* Made the error message shown when failing to load mods show after the main window.
* Made the loading window appear on the screen the main window was on when reloading.

## Mod Info
Made **Size** on the Advanced tab of the Mod information panel available when using -noscanmodfiles for hacks and compiled mods.

## Mod Settings
Fixed an issue where the icon of the Mod Settings window when using `-settings` where the default .NET icon instead of the Mod Launcher's Icon.

## Launcher Settings
Added **Limit to Single Core** to the **Game** tab.

## Localisation
Added support for Language Localization.

# New Hacks
## Lens Flare
Added this new hack. This makes Lens Flares work just like the console releases of the game.

## Video Texture Support
Added this new hack. This allows you to use BIK files as textures.

# Updated Hacks
## Additional Script Functionality
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/AdditionalScriptFunctionality.md }}

## Bug Fixes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/BugFixes.md }}

## Custom Audio Format Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/CustomAudioFormatSupport.md }}

## Custom Files
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/CustomFiles.md }}

## Debug Test
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/DebugTest.md }}

## Debug Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/DebugText.md }}

## Interprocess Communication
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/InterprocessCommunication.md }}

## Modern Computer Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/ModernComputerSupport.md }}

## Resizable Window
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/ResizableWindow.md }}

## Screenshots
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/Screenshots.md }}