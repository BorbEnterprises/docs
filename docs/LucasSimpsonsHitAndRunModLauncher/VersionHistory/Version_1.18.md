---
title: "Version 1.18"
description: "Changelog for Version 1.18 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on July 2, 2018.**

# Launcher
## General
* Added an unhandled exception handler so the Launcher will provide helpful information instead of crashing.
* Changed the order that pressing the tab key cycles through the controls on various windows to be more appropriate.
* Changed the progress bar when loading mods to no longer ease instead of waiting half a second for it to catch up.
* Improved some error messages to be more specific.
* Made mods compiled with no properties in their Miscellaneous section of their Meta.ini able to load.
* Made scanning mod files only include stuff that would be included when compiling (including custom rules in a mod's Compile section).
* Made the entire launcher properly support different DPIs.
* Made the loading window have the Mod Launcher icon in its caption.
* Made the mod launcher support reading command line arguments out of the **CommandLine.txt** placed next to it (if one exists).
    * Command line arguments specified in this file should be separated by new lines.

## Main Window
* Added **Game Install Virtual Store** to the **Open...** menu.
    * This only shows up if the game is on your system drive and a folder for the game exists in your system's [VirtualStore](https://docs.microsoft.com/en-us/previous-versions/technet-magazine/cc138019(v=msdn.10)).
* Fixed the main window not being focused sometimes after loading mods.
* Made **Saved Games** in the **Open...** menu show **Mod Launcher** in brackets if **Always Keep Saved Games Seperate** is enabled.
* Made **Saved Games** and **Screenshots** options in the **Open...** menu show the current Main mod's name in brackets (if one is enabled).

## Mods List
This part of the launcher sees a significant change in this update.

Introducing Pages! This divides mods and hacks into the **General**, **Setting** and **Developer** tabs.

![mod launcher pages](/img/LucasSimpsonsHitAndRunModLauncher/Pages.png)

There's also an **Unreleased** tab which only shows up if there are mods marked as such loaded.

If you're not a fan of this change, you can disable it by right-clicking the mods list and unticking **Pages** to use the old mods list.

Other changes in this version:
* Added an **Enabled Non-favourites** category.
* Added a setting to show enabled mods first in the right-click menu of the Mods list.
* Added the ability to reload individual mod(s) by right clicking them.
    * Not supported on Frameworks at this time.
* Fixed a crash on Wine when selecting mods.
* Made changing the selected mod(s) smoother.
* Made it so the **Output Path Only** and **Decompilable Only** right-click options are not remembered when restarting the Mod Launcher.
* Made the mods list update before the mod load error message is shown.
* Made the watermark work on Windows XP.
* Made ticking and unticking multiple mods smoother.
* When compiling one or more mods, there will now be a window with a cancel button instead of freezing the main window.

## Mods Info
* Made file sizes of mods show 2 decimal places instead of 3 significant figures with the potential of exponents.
* Made mod information not show a **Miscellaneous** category if no categories are defined.
* Made mod information show **No information provided.** if the mod provides none.

## Launcher Settings
Launcher settings got a complete redesign in this version.

There were also the following additions and changes:
* Added **Show Message on Crash** to the Game tab.
* Added **Donut Team Account Integration Support** to the Launcher tab.
    * If you're opted in, this setting can be used to temporarily opt out without removing your credentials.
    * This fully disables this functionality including the button on the main window.
* Added **Close to Tray** to the Launcher tab.
* Added **DPI Aware** to the Launcher tab. This makes the Launcher DPI Aware on Windows 7 or newer.
* Added a `-launchersettings` command line argument that will launch the launcher directly into Launcher Settings.
* Fixed an issue where adding an individual LMLM file in Launcher Settings caused its Title (if there's no Title) and InternalName (if there's no InternalName) to include the LMLM file extension.
    * If you have mods affected by this issue, you will need to remove and re-add them.
* Made **Terminate on Crash** not work if a debugger is attached to the game.
* Made clicking **OK** on the Launcher Settings window only reload mods if any settings that affect mods were changed.
* Made it so licenses are listed in alphabetical order.

## Account Integration
* Changed how the account window is displayed when launching the Mod Launcher for the first time.
* Fixed a random crash when communicating with the Donut Team website.

# Mod Features
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/ModFeatures.md }}

# Updated Mods
## No HUD
Moved this mod to the new **Settings** page.

## No Traffic
Moved this mod to the new **Settings** page.

## Repair Car On Reset
Moved this mod to the new **Settings** page.

## Speedometer
Moved this mod to the new **Settings** page.

## Text Names
Moved this mod to the new **Settings** page.

## Unlock All Rewards
Moved this mod to the new **Settings** page.

# New Hacks
## 3D Phone Booth Preview Support
Added this new hack. This hack adds support for 3D Car Previews in the Phone Booth (similar to those found in Car Shops).

## Additional Script Functionality
Added this new hack. This hack adds several new mission objectives, mission conditions, script commands and other new script functionality.

## Custom Audio Format Support
Added this new advanced hack that allows other hacks to add support for custom audio formats.

## Custom Audio Support
Added this new hack. This allows you to control some audio related features of the game such as starting ambiance for story missions.

## Custom Shop Support
Added this new hack. This hack allows you to specify custom NPCs for car shops and allows you to blacklist or whitelist sars and skins at specific phone booths and skin shops respectively.

## FLAC Support
Added this new hack. This hack adds support for using FLAC files in place of RSD files.

## NVIDIA Highlights
Added this new hack. This hack adds support for NVIDIA Highlights.

## Ogg Vorbis Support
Added this new hack. This hack adds support for using Ogg files in place of RSD files.

# Updated Hacks
## Aspect Ratio Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/AspectRatioSupport.md }}

## Borderless
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/Borderless.md }}

## Bug Fixes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/BugFixes.md }}

## Console
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/Console.md }}

## Custom Car Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/CustomCarSupport.md }}

## Custom Files
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/CustomFiles.md }}

## Debug Checks
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/DebugChecks.md }}

## Debug Hashes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/DebugHashes.md }}

## Debug Test 
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/DebugTest.md }}

## Debug Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/DebugText.md }}

## Discord Rich Presence
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/DiscordRichPresence.md }}

## Flippable Cars
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/DiscordRichPresence.md }}

## Frame Limiter
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/FrameLimiter.md }}

## HUD Map Ignore Player Height
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/HUDMapIgnorePlayerHeight.md }}

## Increased Reward Limits
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/IncreasedRewardLimits.md }}

## Increased Video Resolution Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/IncreasedVideoResolutionSupport.md }}

## Interior Jumping
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/InteriorJumping.md }}

## Interior Kicking
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/InteriorKicking.md }}

## Interior Sprinting
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/InteriorSprinting.md }}

## Modern Computer Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/ModernComputerSupport.md }}

## Multiple Instance Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/MultipleInstanceSupport.md }}

## No Automatic Saved Game Load
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/NoAutomaticSavedGameLoad.md }}

## No Cheats
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/NoCheats.md }}

## No Fast Car Reset
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/NoFastCarReset.md }}

## No Inactive Dynamic Object Collisions
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/NoInactiveDynamicObjectCollisions.md }}

## No Introduction Movies
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/NoIntroductionMovies.md }}

## No Jump Limit
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/NoJumpLimit.md }}

## No Mission Start Cameras
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/NoMissionStartCameras.md }}

## No Time Limits
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/NoTimeLimits.md }}

## Replayable Bonus Missions
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/ReplayableBonusMissions.md }}

## Resizable Window
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/ResizableWindow.md }}

## Screenshots
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/Screenshots.md }}

## Unlock All Missions
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/UnlockAllMissions.md }}

# Removed Hacks
## Custom Car Shop Support
Removed this hack. It is now a `LegacyResource` of the new Custom Shop Support hack.