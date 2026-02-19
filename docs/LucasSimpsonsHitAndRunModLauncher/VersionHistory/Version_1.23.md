---
title: "Version 1.23"
description: "Changelog for Version 1.23 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on May 16, 2019.**

# Launcher
## General
* Added the `-uppercasetext` and `-lowercasetext` command line arguments. These make all the localisable text in the Mod Launcher and messages it shows upper or lower case respectively.
* Made it so file/folder browse dialogues fall back to Windows XP style versions in the event the Mod Launcher or .NET fail to create Windows Vista style dialogues.
  * This resolves an issue where this happened on Windows 10 1809 when using a High Contrast theme.
  * This was also able to happen on Windows 7 with **Disable visual themes** ticked in the executable's compatibility settings.

## Mods List
* Added a **Non-enabled Favourites** category.
* Added a **Descriptionless Hacks** category when using the `-testing` command line argument.
* Added the existing shortcut keys to the right click menu items for **Search...**, **Pages** and **Reload**.

## Launcher Settings
Fixed an issue where **Copy Require Line** was disabled in the right click menu of **Hack Support** on the **Non-mod Hacks** page (which is only visible with **Show Advanced Hacks** ticked).

## Account Integration
Added the `-nodtcomms` command line argument. This disables Donut Team Account Integration.

## Localisation
There are some fixes and improvements to localisation in this version as well as new strings.
* Fixed an issue where the **Jump List** tickbox on the **Manage Configurations...** window did not correctly handle being repositioned/resized with language localisation.
* Made non-ingame messages from the Custom Files, Custom Save Data, Debug Test and Screenshots hacks support language localisation.

A new template language (Template_1.23.xml) was published on [Project:181] including all the new strings.

# New Hacks
## Custom Controller Support
Added this new advanced hack that other hacks can use to extend the game's controller support.

## Direct3D 9
Added this new hack that makes the game use Direct3D 9 instead of Direct3D 8.

This may be helpful when trying to use 3rd party tools such as ReShade.

## XInput
Added this new hack that makes the game use XInput instead of DirectInput for controllers/gamepads.

This has various advantages over DirectInput:
* Makes controller rumble work.
  * This can be disabled in the hack's settings.
* Makes the game compatible with Steam's controller support when launching the Mod Launcher through Steam as a non-Steam game.
* Makes it so you can plug in new controllers while the game is running.

Currently, DirectInput only controllers will not work with this hack enabled and only one trigger can be used at a time. You can bind actions to both but they cannot be pressed at the same time.

# Updated Hacks
## Hack Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/HackSupport.md }}

## Anti-aliasing
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/Antialiasing.md }}

## Aspect Ratio Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/AspectRatioSupport.md }}

## Cancellable Initial Walk
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/CancellableInitialWalk.md }}

## Custom Audio Format Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/CustomAudioFormatSupport.md }}

## Custom Main Menu Items
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/CustomMainMenuItems.md }}

## Custom Save Data
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/CustomSaveData.md }}

## Discord Rich Presence
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/DiscordRichPresence.md }}

## Dynamic Tree Node Entity Limits
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/DynamicTreeNodeEntityLimits.md }}

## Force Mission Select Level Reload
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/ForceMissionSelectLevelReload.md }}

## Frame Limiter
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/FrameLimiter.md }}

## HUD Map Ignore Player Height
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/HUDMapIgnorePlayerHeight.md }}

## Interprocess Communication
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/InterprocessCommunication.md }}

## Lens Flare
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/LensFlare.md }}

## Letterbox
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/Letterbox.md }}

## Lua Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/LuaSupport.md }}

## Mirror Mode
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/MirrorMode.md }}

## No Cheats
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/NoCheats.md }}

## No Cursor Until Mouse Move
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/NoCursorUntilMouseMove.md }}

## No Fast Car Reset
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/NoFastCarReset.md }}

## No Go To Objective Camera Focus
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/NoGoToObjectiveCameraFocus.md }}

## No Introduction Movies
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/NoIntroductionMovies.md }}

## No Jump Limit
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/NoJumpLimit.md }}

## No Mission Start Cameras
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/NoMissionStartCameras.md }}

## No Mute on Defocus
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/NoMuteOnDefocus.md }}

## No Pause on Defocus
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/NoPauseOnDefocus.md }}

## No Suppressed Drivers
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/NoSuppressedDrivers.md }}

## NVIDIA Highlights
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/NVIDIAHighlights.md }}

## One Tap Player Car Death
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/OneTapPlayerCarDeath.md }}

## Replayable Bonus Missions
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/ReplayableBonusMissions.md }}

## Road Names
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/RoadNames.md }}

## Skip Main Menu
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/SkipMainMenu.md }}

## Skippable Start Cameras
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/SkippableStartCameras.md }}

## Starting Coins
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/StartingCoins.md }}


