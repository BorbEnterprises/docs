---
title: "Version 1.25.1"
description: "Changelog for Version 1.25.1 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on August 1, 2020.**

# Launcher
## General
* Improved performance when working out what mod icon should be shown for configurations that don't have a main mod enabled on the main window, in the right click menu of the mods list, on the Manage Configurations window and when updating the Jump List.
* Made it so the configurations list in the right click menu of the mods list is only updated when opening the menu after one of the following circumstances has occurred since it was last opened:
	* Changing what main mods or edition mods are enabled for the current configuration.
	* Reloading mods.
	* Pressing "OK" on the "Manage Configurations" window.

## Mod Settings
Fixed an issue introduced in Version 1.24 where having a single mod setting with a wide label in a group or page by itself caused it to be smaller than it's supposed to be.

## Configurations
Fixed an issue where the Main mod or Edition mod's icon would not appear on the "Manage Configurations" window when importing a configuration that had a Main mod or an Edition mod enabled until the window was closed and re-opened.

# Mod Features
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25.1/ModFeatures.md }}

# Updated Hacks
## Hack Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25.1/Hacks/HackSupport.md }}

## Additional Script Functionality
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25.1/Hacks/AdditionalScriptFunctionality.md }}

## Debug Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25.1/Hacks/DebugText.md }}