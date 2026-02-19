---
title: "Version 1.24"
description: "Changelog for Version 1.24 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on May 19, 2020.**

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
Fixed an issue where settings with wide labels could cause all but the last setting in their group to overflow the group.

## Launcher Settings
* Made "Show License" on the right click menu of hacks on the Non-mod Hacks page only include the licenses of advanced hacks they require when "Show Advanced Hacks" is unticked.
* Fixed an issue where settings that were not set to their default value would not be bold when opening the window if this meant they were unticked.

## Localisation
This version adds new language strings.

A new template language (Template_1.24.xml) was published on [Project:181] including these new strings at the end of the file.

# New Hacks
## File System RCFs
Added this new hack.

## No Audio
Added this new hack.

The **No Audio** mod is still included but it is overridden by this hack unless you explicitly disable the hack with the `-disablehack` NoAudio command line argument.

# Updated Hacks
## Hack Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/HackSupport.md }}

## Bug Fixes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/BugFixes.md }}

## Custom Car Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomCarSupport.md }}

## Custom Character Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomCharacterSupport.md }}

## Custom Files
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles.md }}

### Custom Limits
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomLimits.md }}

### Custom Stats Totals
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomStatsTotals.md }}

### Custom Vertex Shader Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomVertexShaderSupport.md }}

## Debug Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/DebugText.md }}

## FLAC Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/FLACSupport.md }}

## Interior Sprinting
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/InteriorSprinting.md }}