---
title: "Version 1.20"
description: "Changelog for Version 1.20 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on December 22, 2018.**

# Highlights
* New Custom Trigger Actions hack for binding custom actions to triggers.
* New mission commands in ASF for toggling pedestrians and parked cars for missions.
* Several new setting hacks including a fancy Letterbox hack.

# Launcher
## General
* Added the `-nocommandlinefile` command line argument.
* Added the `-nodeleteold` command line argument.
* Added the `-ignorelaunchmodconflicts` command line argument.
* Added the `-nowatermark` command line argument.
* Fixed an issue where ampersands were incorrectly escaped for the tray icon hover text.
* Made launching the game detect types of conflicts that previously were only detected when ticking mods.
* Made the `-allowignoremodconflicts` command line argument also allow the user to ignore conflicts detected when launching the game.

## Main Window
Made **Close Launcher** default to being unticked (based on the results of a poll).

## Localization
This version introduces a new language string for when a conflict is detected upon launching the game.

A new template language (Template_1.20.xml) was published on [Project:181] including these new string formats as well as the original strings. The template also now indicates when strings were removed if they were in this update or any previous ones.

# New Hacks
## Cancellable Initial Walk
Added this new hack that allows you to interrupt the character walking at the start of a level.

## Custom Trigger Actions
Added this new hack. This allows you to bind various custom actions to specific triggers or events with optional conditions.

## Letterbox
Added this new hack that allows you to force the game into a specific aspect ratio regardless of the game window's dimensions.

This may prove helpful for speedrunners who want to maximize their game window or play in full screen while forcing the game into 4:3.

## No Go To Objective Camera Focus
Added this new hack that disables the game taking control of the camera when you step near the target on foot in a `goto` stage.

## No Main Menu Camera Animations
Added this new hack that disables the camera animations on the main menu.

This hack is requirable as well if a mod calls for it.

## No Wrenches
Added this new hack that fully disables wrenches.

## One Tap Player Car Death
Added this new hack that makes the player's car get destroyed in one hit.

This hack has various options for what types of thing annihilate the player's car.

# Updated Hacks
## Additional Script Functionality
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.20/Hacks/AdditionalScriptFunctionality.md }}

## Aspect Ratio Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.20/Hacks/AspectRatioSupport.md }}

## Debug Test
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.20/Hacks/DebugTest.md }}

## Debug Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.20/Hacks/DebugText.md }}

## Lens Flare
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.20/Hacks/LensFlare.md }}