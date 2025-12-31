---
title: Version 1.18
description: "This update was released on July 2nd, 2018."
authors: ["loren","lucasc190"]
---

**This update was released on July 2nd, 2018.**

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
* Made the mod launcher support reading command line arguments out of the "CommandLine.txt" placed next to it (if one exists).
    * Command line arguments specified in this file should be separated by new lines.

## Main Window

* Added "Game Install Virtual Store" to the "Open..." menu.
    * This only shows up if the game is on your system drive and a folder for the game exists in your system's [VirtualStore](https://docs.microsoft.com/en-us/previous-versions/technet-magazine/cc138019(v=msdn.10)).
* Fixed the main window not being focused sometimes after loading mods.
* Made "Saved Games" in the "Open..." menu show "Mod Launcher" in brackets if "Always Keep Saved Games Seperate" is enabled.
* Made "Saved Games" and "Screenshots" options in the "Open..." menu show the current Main mod's name in brackets (if one is enabled).

## Mods List
This part of the launcher sees a significant change in this update.

Introducing Pages! This divides mods and hacks into the "General", "Setting" and "Developer" tabs.

![mod launcher pages](/img/lucasmodlauncher/misc/pages.png)

There's also an "Unreleased" tab which only shows up if there are mods marked as such loaded.

If you're not a fan of this change, you can disable it by right-clicking the mods list and unticking "Pages" to use the old mods list.

Other changes in this version:

* Added an "Enabled Non-favourites" category.
* Added a setting to show enabled mods first in the right-click menu of the Mods list.
* Added the ability to reload individual mod(s) by right clicking them.
    * Not supported on Frameworks at this time.
* Fixed a crash on Wine when selecting mods.
* Made changing the selected mod(s) smoother.
* Made it so the "Output Path Only" and "Decompilable Only" right-click options are not remembered when restarting the Mod Launcher.
* Made the mods list update before the mod load error message is shown.
* Made the watermark work on Windows XP.
* Made ticking and unticking multiple mods smoother.
* When compiling one or more mods, there will now be a window with a cancel button instead of freezing the main window.

## Mods Info

* Made file sizes of mods show 2 decimal places instead of 3 significant figures with the potential of exponents.
* Made mod information not show a "Miscellaneous" category if no categories are defined.
* Made mod information show "No information provided." if the mod provides none.

## Launcher Settings
Launcher settings got a complete redesign in this version.

There were also the following additions and changes:

* Added "Show Message on Crash" to the Game tab.
* Added "Donut Team Account Integration Support" to the Launcher tab.
    * If you're opted in, this setting can be used to temporarily opt out without removing your credentials.
    * This fully disables this functionality including the button on the main window.
* Added "Close to Tray" to the Launcher tab.
* Added "DPI Aware" to the Launcher tab. This makes the Launcher DPI Aware on Windows 7 or newer.
* Added a "-launchersettings" command line argument that will launch the launcher directly into Launcher Settings.
* Fixed an issue where adding an individual LMLM file in Launcher Settings caused its Title (if there's no Title) and InternalName (if there's no InternalName) to include the LMLM file extension.
    * If you have mods affected by this issue, you will need to remove and re-add them.
* Made "Terminate on Crash" not work if a debugger is attached to the game.
* Made clicking "OK" on the Launcher Settings window only reload mods if any settings that affect mods were changed.
* Made it so licenses are listed in alphabetical order.

## Account Integration

* Changed how the account window is displayed when launching the Mod Launcher for the first time.
* Fixed a random crash when communicating with the Donut Team website.

# Mod Features

* Added `General`, `Setting`, `Developer` and `Unreleased` properties to the `[Miscellaneous]` section to control which page a mod is listed on in the Mods List.
* Added the `[LegacyResource]` section which allows mods to supersede other mods.
* Added support for multiple `InternalName` properties.
* Added support for `Colour` type settings.
* Made the `Default` property on `Text` type settings optional instead of causing a crash when it's omitted.

# Hacks

## General
The following hacks were moved to the new Settings page:

* Aspect Ratio Support
* Borderless
* Bug Fixes
* Discord Rich Presence
* Flippable Cars
* Frame Limiter
* HUD Map Ignore Player Height
* Interior Jumping
* Interior Kicking
* Interior Sprinting
* Multiple Instance Support 
    * Also no longer hidden by default.
* No Automatic Saved Game Load
* No Cheats 
    * Also no longer hidden by default.
* No Fast Car Reset
* No Inactive Dynamic Object Collisions
* No Introduction Movies
* No Jump Limit
* No Mission Start Cameras
* No Time Limits
* Replayable Bonus Missions
* Resizable Window
* Screenshots
* Unlock All Missions

The following mods were moved to the new Settings page:

* No HUD
* No Traffic
* Repair Car On Reset
* Speedometer
* Text Names
* Unlock All Rewards

The following hacks were moved to the new Developer page:

* Console
* Debug Checks
* Debug Hashes
* Debug Test 
    * Also no longer hidden by default.
* Debug Text

The following new hacks were added to the Settings page:
   
* Force Mission Select Level Reload
* No Cursor Until Mouse Move
* No Mute on Defocus
* No Pause on Defocus
* Skip Main Menu
* Skippable Start Cameras
* Starting Coins

## 3D Phone Booth Preview Support
Added this new hack. This hack adds support for 3D Car Previews in the Phone Booth (similar to those found in Car Shops).

## Additional Script Functionality
Added this new hack. This hack adds several new mission objectives, mission conditions, script commands and other new script functionality.

## Aspect Ratio Support

* Added a new FOV mode called "Average".
* Fixed an issue that caused the aspect ratio to start off corrupt if the Resizable Window hack's "Start Maximised" setting was enabled.

## Bug Fixes

* Added a fix for a crash related to the options menu and the Unlock All Cameras cheat.
* Added a fix for the crash that happens if the game is not focused fast enough on the license screen.
* Moved the Main Menu Cheat Code Enter crash fix to the new Crashes group.

## Custom Audio Support
Added this new hack. This allows you to control some audio related features of the game such as starting ambiance for story missions.

## Custom Audio Format Support
Added this new advanced hack that allows other hacks to add support for custom audio formats.

## Custom Car Support
Added the `PreviewScale` property. This allows you to set a custom scale for the car when it's in a car shop.

## Custom Car Shop Support
Removed this hack. It is now a `LegacyResource` of the new Custom Shop Support hack.

## Custom Files
Added a third argument to the `DirectoryGetEntries` function called "EndToStart" which returns the list of files and folders in reverse order.

## Custom Shop Support
Added this new hack. This hack allows you to specify custom NPCs for car shops and allows you to blacklist or whitelist sars and skins at specific phone booths and skin shops respectively.

## Debug Checks

* Made the hack use Radical's official chunk names.
    * You can revert to the old names by using the new "Use Legacy Names" setting in the hack's settings.
* Made "Experimental Missing Locator Detection" work outside the Release English version of the game.

## Debug Test
### Menus Page

* Removed "Force Mission Select Level Reload".
* Removed "No Cursor Until Mouse Move".

### Graphics Page
Added "Default Resolution". This allows you to configure the default resolution of the game window before the game loads your settings.

### Debug Page
* Removed "Ignore Suppressed Drivers".
* Removed "Starting Coins".

### Vehicles Page
Added "No Destroyed Car Jump Out".

### Audio Page

* Added "Force Level RMS". This setting allows you to force a specific level's RMS file to always be loaded/used.
* Added "No Pause Audio Fade".

### Miscellaneous Page

* Added "Disable Window Ghosting".
* Added "No Handle File Not Found".
* Added "Use Camera Position".
* Added "No Animated Camera Letterbox".
* Added "Use Tracking Heaps".
* Removed "No Suppressed Drivers" (yes, there were two of these settings).

### Other

* Made the K Key reload the music RMS file and trigger an event named "Test" if it exists.
* Made Shift+F10 fail the first condition of the active stage (if the stage has any conditions).

## Debug Text
### General

* Added settings that allow you to configure the look and feel of the hack and which pages are visible.
* Fixed lag on the "dyna phys" and "static phys" pages while loading.
* Made the hack work during movies.
* Made the hack use Radical's official chunk names.
    * You can revert to the old names by using the new "Use Legacy Names" setting on the Advanced tab of the hack's settings.
* Made the "car joints" and "character joints" pages show the joints in the world instead of listing them.
* Made the hack check for a font called "DebugText" and use that if it exists.

### "car matrix" Page
Added this page.

### "memory" Page
Added this page with information on a few different heaps.

### "music" Page
Added this page with various information about the currently loaded RMS files.

### "regions" Page
Made this page also show the current and loaded interior.

### "road segments" Page
Added this page that draws road segments in the world with names.

### "root tree node and animated icons" Page

* Fixed a crash when going to this page when not ingame or while loading.
* Made "Animated icons" work outside the Release English version of the game.

### "traffic" Page
Made "Contact car traffic locomotion AI segment" now include the road segment name in brackets.

### "triggers" Page
Made this page list triggers the player is in and show triggers as boxes with names in the world.

## FLAC Support
Added this new hack. This hack adds support for using FLAC files in place of RSD files.

## Increased Reward Limits

* Made it so the game won't get corrupt when trying to add more than 60 car health values to the save file. It now shows an assert message when trying to add more than 60 (except for when the mod is being used in Multiplayer).
* Removed the assert when trying to add more than 60 reward cars.
* Removed the limit of 64 reward cars.
    * **NOTE:** There is still a limit of 64 cars in one phonebooth but you can use CustomShopSupport to spread the cars across multiple phonebooths.

## Increased Video Resolution Support
This hack now removes memory restrictions when playing RMV files.

## Modern Computer Support
Made non-english versions of the game use 200,000hz as the maximum sample rate like the Release English version instead of 100,000hz.

## NVIDIA Highlights
Added this new hack. This hack adds support for NVIDIA Highlights.

## Ogg Vorbis Support
Added this new hack. This hack adds support for using Ogg files in place of RSD files.

## Screenshots

* Fixed an issue where the default screenshot sound did not work on Windows XP.
* Fixed this hack failing to take screenshots on Wine or Oracle VM VirtualBox Guest Additions.