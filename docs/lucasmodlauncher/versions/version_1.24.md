---
title: Version 1.24
description: "This update was released on May 19th, 2020."
authors: ["loren","lucasc190"]
---

**This update was released on May 19th, 2020.**

# Launcher
## General

* Added the `-randomcasetext`, `-invertcasetext`, `-alternatingcasetext` and `-reversetext` command line arguments.
* Made "Show License" on the right click menu of hacks (in the mods list and on the Non-mod Hacks page of the Launcher Settings window) not include the license(s) of Hack Support.
	* Only when its a required advanced hack. This does not affect Hack Support itself.
	* This prevents hacks that don't use TinyXML from including TinyXML in this menu.
		* This was an issue introduced in 1.22.4.
* Fixed another crash on startup when failing to read/write a pinned shortcut.
	* The `-nofixpinnedshortcuts` command line argument could be used to workaround this.

## Mods List

* Made it so the sub category combo box gets cleared if the selected category has no sub categories.
* Made it reloading individual mods keeps them selected.

## Mod Settings

* Fixed an issue where settings with wide labels could cause all but the last setting in their group to overflow the group.

## Launcher Settings

* Made "Show License" on the right click menu of hacks on the Non-mod Hacks page only include the licenses of advanced hacks they require when "Show Advanced Hacks" is unticked.
* Fixed an issue where settings that were not set to their default value would not be bold when opening the window if this meant they were unticked.

## Localisation
This version adds new language strings.

A new template language (Template_1.24.xml) was published on [this page](../localisation.md) including these new strings at the end of the file.

# Hacks
## Hack Support
{{ snippet lucasmodlauncher/versions/1.24/hack_hack-support }}

## Bug Fixes
{{ snippet lucasmodlauncher/versions/1.24/hack_bug-fixes }}

## Custom Car Support
{{ snippet lucasmodlauncher/versions/1.24/hack_custom-car-support }}

## Custom Character Support
{{ snippet lucasmodlauncher/versions/1.24/hack_custom-character-support }}

## Custom Files
{{ snippet lucasmodlauncher/versions/1.24/hack_custom-files }}

## Custom Limits
{{ snippet lucasmodlauncher/versions/1.24/hack_custom-limits }}

## Custom Stats Totals
{{ snippet lucasmodlauncher/versions/1.24/hack_custom-stats-totals }}

## Custom Vertex Shader Support
{{ snippet lucasmodlauncher/versions/1.24/hack_custom-vertex-shader-support }}

## Debug Text
{{ snippet lucasmodlauncher/versions/1.24/hack_debug-text }}

## File System RCFs
Added this new hack.

## FLAC Support
{{ snippet lucasmodlauncher/versions/1.24/hack_flac-support }}

## Interior Sprinting
{{ snippet lucasmodlauncher/versions/1.24/hack_interior-sprinting }}

## No Audio
Added this new hack.

The "No Audio" mod is still included but it is overridden by this hack unless you explicitly disable the hack with the `-disablehack NoAudio` command line argument.