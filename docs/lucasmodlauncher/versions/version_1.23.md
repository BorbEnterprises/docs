---
title: Version 1.23
description: "This update was released on May 16th, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on May 16th, 2019.**

# Launcher
## General

* Added the `-uppercasetext` and `-lowercasetext` command line arguments. These make all the localisable text in the Mod Launcher and messages it shows upper or lower case respectively.
* Made it so file/folder browse dialogues fall back to Windows XP style versions in the event the Mod Launcher or .NET fail to create Windows Vista style dialogues.
    * This resolves an issue where this happened on Windows 10 1809 when using a High Contrast theme.
    * This was also able to happen on Windows 7 with "Disable visual themes" ticked in the executable's compatibility settings.

## Mods List

* Added a "Non-enabled Favourites" category.
* Added a "Descriptionless Hacks" category when using the `-testing` command line argument.
* Added the existing shortcut keys to the right click menu items for "Search...", "Pages" and "Reload".

## Launcher Settings
Fixed an issue where "Copy Require Line" was disabled in the right click menu of "Hack Support" on the "Non-mod Hacks" page (which is only visible with "Show Advanced Hacks" ticked).

## Account Integration
Added the `-nodtcomms` command line argument. This disables Donut Team Account Integration.

## Localisation
There are some fixes and improvements to localisation in this version as well as new strings.

* Fixed an issue where the "Jump List" tickbox on the "Manage Configurations..." window did not correctly handle being repositioned/resized with language localisation.
* Made non-ingame messages from the Custom Files, Custom Save Data, Debug Test and Screenshots hacks support language localisation.

A new template language (Template_1.23.xml) was published on [this page](../localisation.md) including all the new strings.

# Hacks
## General
Added descriptions to the following hacks:

* Anti-aliasing
* Cancellable Initial Walk
* Dynamic Tree Node Entity Limits
* Force Mission Select Level Reload
* Lens Flare
* Letterbox
* Mirror Mode
* No Cursor Until Mouse Move
* No Go To Objective Camera Focus
* No Mute on Defocus
* No Pause on Defocus
* No Suppressed Drivers
* One Tap Player Car Death
* Skip Main Menu
* Skippable Start Cameras
* Starting Coins

Updated the descriptions of the following hacks:

* Discord Rich Presence
* Frame Limiter
* HUD Map Ignore Player Height
* NVIDIA Highlights
* No Cheats
* No Fast Car Reset
* No Introduction Movies
* No Jump Limit
* No Mission Start Cameras
* Replayable Bonus Missions

Made it so the following hacks can no longer be required by mods:

* Ambient Car Support
* Aspect Ratio Support
* Custom Audio Format Support
* Custom Main Menu Items
* Custom Save Data
* Interprocess Communication
* Lua Support
* Road Names

Attempting to require these hacks in a mod that doesn't have a `RequiredLauncher` specified or has `RequiredLauncher` set to a version lower than 1.23 will be ignored for backwards compatibility reasons.

## Hack Support

* Added the `-hookd3d` command line argument.
* Added the `-nohandlefilenotfound` command line argument.
* Added the `-nohardwareskinning` and `-hardwareskinning` command line arguments.
* Added the `-noreloadcarcameradata` command line argument.
* Fixed an issue where the Direct3D hook in this hack caused the game to reset the Direct3D device redundantly once at startup.
* Made this hack block the game from resetting the Direct3D device when it's not nessecary.
    * Also added the `-noblockredundantreset` command line argument to opt out of this.
* Made the game terminate abruptly with no message or crash dump in the case that an exception occurs in the hack window procedure event (instead of letting Windows swallow the exception and likely cause corruption).

## Custom Controller Support
Added this new advanced hack that other hacks can use to extend the game's controller support.

## Direct3D 9
Added this new hack that makes the game use Direct3D 9 instead of Direct3D 8.

This may be helpful when trying to use 3rd party tools such as ReShade.

## Lens Flare

* Made this hack work differently (using an [occlusion query](https://docs.microsoft.com/en-us/windows/win32/direct3d9/queries) instead of a lockable render target) when using Direct3D 9.
    * Also added a `-noocclusion` command line argument to opt out of this.
    * Also added a `-occlusionsleep` command line argument.

## No Cursor Until Mouse Move
Made this hack only show the cursor if it moves more than 5 pixels on either axis. This tolerance is customisable in the hack's settings (0 meaning any movement and -1 meaning the old behaviour where it will show up any time the window receives a mouse move event even if the cursor's position doesn't change).

## Resizable Window

* Added the `-nomaintainwindowcentre` command line argument. This prevents this hack from trying to maintain the centre point of the game window when the game resizes it.
* Made the game terminate abruptly with no message or crash dump in the case that an exception occurs in the resizing timer callback (instead of letting Windows swallow the exception and likely cause corruption).
* Made this hack check if the game window is currently maximised instead of checking if the "Start Maximised" setting is ticked before suppressing the changing of the resolution when the game loads its settings.
* Made this hack update the game's unmaximised size and position if the game is maximised when it loads its settings.
* Made this hack force the game window to fit within the working area of the screen it's on when maintaining the window centre when the game resizes its window.
* Made this hack prevent you from resizing the client area of the game below 1 pixel on the width or height.
    * Also added a "-allowzerowindowsize" to opt out of this.
* No longer resizes or repositions the window if the resolution changes when the game is in full screen.
    * This became an issue with Hack Support blocking the game from resetting its Direct3D device redundantly in this version.
* No longer maintains the centre of the window when changing out of full screen.
* No longer handles resizing when the game is in full screen.

## Screenshots
Improved error handling.

## XInput
Added this new hack that makes the game use XInput instead of DirectInput for controllers/gamepads.

This has various advantages over DirectInput:

* Makes controller rumble work.
    * This can be disabled in the hack's settings.
* Makes the game compatible with Steam's controller support when launching the Mod Launcher through Steam as a non-Steam game.
* Makes it so you can plug in new controllers while the game is running.
   
Currently, DirectInput only controllers will not work with this hack enabled and only one trigger can be used at a time. You can bind actions to both but they cannot be pressed at the same time.