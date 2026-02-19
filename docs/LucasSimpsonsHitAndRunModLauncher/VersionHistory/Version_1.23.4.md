---
title: "Version 1.23.4"
description: "Changelog for Version 1.23.4 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on September 1, 2019.**

# Highlights
Two new mod hacks that reintroduce features from the console versions of the game:
* Hover Car Refraction
* Sphere Maps

# Launcher
## General
* Added a check for if you have Service Pack 3 installed when using Windows XP.
  * Also added the `-forcexpsp3check`, `-noxpsp3check` and `-spoofxpsp3check` command line arguments.
* Added the `-ignoreloaderrors` command line argument. This makes the Mod Launcher ignore errors when loading mods and hacks.

## Main Window
Fixed an issue where the update link still left a gap for the Account button when Donut Team Account Integration was disabled.

## Localisation
This version adds a couple new language strings related to the new Service Pack 3 check on Windows XP.

A new template language (Template_1.23.4.xml) was published on [Project:181] including these new strings at the end of the file.

# New Hacks
## Custom Vertex Shader Support
Added this new advanced hack.

## Hover Car Refraction
Added this new Setting mod hack. This reimplements the refraction effect for Professor Frink's Hover Car from the console versions of the game. This reimplementation is based on the Xbox version.

## Refraction Shader Support
Added this new advanced hack. This reimplements the refract PDDI shader type from the console versions of the game.

## Sphere Maps
Added this new Setting mod hack. This improves reflections on cars by reimplementing the spheremap PDDI shader type from the console versions of the game. This reimplementation is based on the Xbox version.

By default, all spheremap shaders are remapped to be environment shaders on PC and this hack undoes that.

# Updated Hacks
## Additional Script Functionality
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.4/Hacks/AdditionalScriptFunctionality.md }}

## Bug Fixes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.4/Hacks/BugFixes.md }}

## Custom Limits
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.4/Hacks/CustomLimits.md }}

## Debug Checks
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.4/Hacks/DebugChecks.md }}

## Debug Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.4/Hacks/DebugText.md }}

## Lens Flare
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.4/Hacks/LensFlare.md }}

## Override Shader Parameters
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.4/Hacks/OverrideShaderParameters.md }}