---
title: "Version 1.23.2"
description: "Changelog for Version 1.23.2 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on July 29, 2019.**

# Launcher
## General
* Made it so Windows messages about the game process failing to start will get shown (such as when a DLL is missing).
* Made it so the message from the `-debuglaunch` command line argument will no longer show up a second time if mods or hacks change in such a way that the Mod Launcher reloads all mods and hacks before starting the game.

## Mods List
* Fixed an issue where mods that were enabled by default and then disabled by the user would become enabled again when unticking "Defaults" for the configuration or when they're no longer enabled by default (which can happen when they're updated).
* Fixed an issue where mods that were hidden by default then unhidden by the user would become hidden again when they're no longer set to be hidden by default (which can happen when they're updated).
* Made it so ticking a mod that conflicts with multiple enabled mods will show a message for each conflicting mod.
* Made it so the `-nounreleased` command line argument doesn't prevent the warning message shown when compiling mods that are marked as unreleased.

## Mod Settings
Fixed an issue where these windows allowed enough space for the widest label next to the widest input control even if they were in different groups.

## Localisation
This version adds a few new language strings.

A new template language (Template_1.23.2.xml) was published on [Project:181] including these new strings at the end of the file.

# Mod Features
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/ModFeatures.md }}

# New Mods
## No Audio
Added this mod.

# New Hacks
## Load Manager Thread Coordination
Added this new advanced hack.

## No Renderer
Added this awesome new setting hack. It's hidden by default.

# Updated Hacks
## Hack Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/Hacks/HackSupport.md }}

## Aspect Ratio Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/Hacks/AspectRatioSupport.md }}

## Custom Controller Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/Hacks/CustomControllerSupport.md }}

## Debug Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/Hacks/DebugText.md }}

## Direct3D 9
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/Hacks/Direct3D9.md }}

## Frame Limiter
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/Hacks/FrameLimiter.md }}

## Lens Flare
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/Hacks/LensFlare.md }}

## Modern Resolution Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.2/Hacks/ModernResolutionSupport.md }}