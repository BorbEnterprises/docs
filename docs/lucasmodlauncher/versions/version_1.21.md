---
title: Version 1.21
description: "This update was released on January 20th, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on January 20th, 2019.**

# Highlights

* **Anti-Aliasing Hack**: A new stand-alone hack for anti-aliasing.
* **Configurations**: Save and load sets of enabled mods and mod settings to make it easier to switch between them.
* **Mod Search**: Easily search the Mods List with Ctrl+F.

# Launcher
## General

* Added `-disablehack` command line argument to prevent a specific hack from being loaded by its name.
* Added `-font` command line argument to allow the use of custom fonts.
* Added `-fontscale` command line argument back which was inexplicably removed in 1.19.
* Added `-ignorerequiredsystem` command line argument which allows hacks that do not support the host operating system to be loaded and enabled.
* Added `-nocheckmodchanges` command line argument to make it so the Mod Launcher doesn't keep track of Meta.ini files changing.
* Added `-nocloselaunchertickbox` command line argument to hide the "Close Launcher" tickbox.
* Added `-spoofdotnetcheck` command line argument.
* Changed the way the Mod Launcher detects if a Meta.ini was changed.
    * Previously, it detected this by checking if the modified date was newer than when the mod was loaded.
    * Now, it detects this by checking if the modified date is different than what it was when the mod was loaded.
    * This resolves an issue where extracting files from a ZIP/RAR made in a timezone that's "in the future" would cause the launcher to think the file changed every time it went to check it.
* Fixed the .NET 3.5 check added in 1.18 that was broken in 1.19.
* Fixed a crash when launching the game with a negative value in an integer setting.
* Made launching show a prompt to reload mods if their Meta.ini file changed since they were loaded.
* Made loading resources out of hacks more efficient.
* Made the `-allowignoremodconflicts` command line argument allow ignoring required mods.
* Made the launcher delete the Hacks folder next to it if it's empty after deleting old hacks.
* Made the launcher check that you're running Windows XP or later so it can show a special message if you try running it on [Windows 98](/img/lucasmodlauncher/misc/windows98_message.png) or [Windows 2000](/img/lucasmodlauncher/misc/windows2000_message.png) with .NET 2.0 installed.
* Made the launcher show a more clear message when trying to load a mod that doesn't exist.
* Made it so if the text of the tray icon exceeds 63 characters, it gets shortened.
* Made showing stuff in Explorer still open the containing folder and select the stuff that does exist even if some of it doesn't.

## Mods List

* Added search, accessible via the right click menu of the Mods List and with Ctrl+F or F3 on the main window. It can be closed with the escape key while the text box is focused.
* Added a "Default" category that shows mods that are enabled by default.
* Added a Ctrl+P shortcut to toggle pages.
* Added "Show License" to the right click menu of mod hacks that have licenses.
* Fixed an issue where reloading individual mods caused the Mod Launcher to try and load all the hacks again.
* Fixed an issue where you could trick the Mod Launcher into reloading frameworks by changing their Meta.ini and compiling them.
* Fixed an issue where the separator line under "Pages" in the right click menu of the Mods List was hidden on the "Settings" page.

## Launcher Settings

* Added "Show License" to the right click menu of mods on the "Non-mod Hacks" tab that have licenses.
* Made the "Executable Path" text box support dragging a folder or executable onto it to set the game executable/directory.
* Made the "Additional Mods > Mods Folders" list support dragging folders onto it to add them to the list.
* Made the "Additional Mods > Mods Folders" list support removing folders with the delete key.
* Made the "Additional Mods > Individual Mods" list support dragging folders or LMLM files onto it to add them to the list.
* Updated the Lua license.
* Updated the libpng license.
* Updated the zlib license.
* Renamed the "Discord" license to "Discord RPC".
* Renamed the "NVIDIA" license to "GeForce Experience SDK".
* Renamed the "OpenSSL" license to "LibreSSL".

## Configurations

* Added Configurations, manage and switch between them from the right click menu of the Mods List.
    * The title of the currently enabled one will be added to the title of the main window.
    * The Donut Team account used to sign into the Mod Launcher is shared across all configurations.
    * Also added a `-configuration` command line argument to launch the Mod Launcher with a specific configuration enabled.
        * This can be used in conjunction with "-launch" to launch directly into a configuration you've set up.
        * This does not change the configuration you have set.
    * Also added a `-notitleconfiguration` command line argument to make it so the current configurations title will not be added to the window title.

# Hacks
## General
Combined all hacks into a single DLL, Hacks.dll, that is now located in the DLLs folder.

Hacks are still individually active (meaning they patch game code and communicate with other hacks) when enabled via the same logic as before (required by mods, enabled in the Mods List, etc).

## Anti-aliasing
Added this new setting hack that allows you to use anti-aliasing if it's supported by your graphics card. If any are supported, it defaults to the highest one but if none are supported, this hack will not show up in the mods list.

You can use "-nomsaa" to have the launcher skip checking what MSAA modes your graphics card supports and disable the hack and hide it from the mods list.

You can also use "-forcemsaa" to have the launcher skip checking what MSAA modes your graphics card supports and force the hack to be in the mods list with all of the possible MSAA modes listed.

## Aspect Ratio Support
Changed the default "FOV > Mode" from "Fit" to "Average".

## Additional Script Functionality
Removed "!m_bStart" asserts (previously on lines [3292](/img/lucasmodlauncher/misc/asf_bStart_3292.png) and [3336](/img/lucasmodlauncher/misc/asf_bStart_3336.png)) related to using the `SetPedsEnabled` and `SetParkedCarsEnabled` commands respectively.

## Bug Fixes
Renamed "Fix Late Focus Freeze" to "Late Focus Freeze".

## Custom Main Menu Items
Added this new advanced hack to centralize code related to main menu modifications made by Debug Test, Multiplayer and No Saved Games.

Mods cannot currently configure this hack.

## Custom Trigger Actions

* Fixed an oversight where this hack was marked as Advanced.
* Fixed an oversight where this hack was still marked as Unreleased.

## Debug Test
### Graphics Page
Removed "Anti-aliasing".

### Vehicles Page
Fixed an issue where "Target Player > Traffic" did not work in the Best Sellers Series version of the game.

### Miscellaneous Page
Fixed a mistake where "Delta Time" was mislabeled to as "Substeps" (a different concept).

## Debug Text
### "gags" Page
Added this page. It lists all the current gags (the outside ones or the ones for the current interior) and whether or not they're loading/loaded. It also shows their joint positions in the world.

## Discord Rich Presence

* Fixed an oversight where the hack was listed on Windows XP.
* Updated to a newer version of Discord RPC.

## Frame Limiter
Added a new "Method" setting for controlling how the frame limiting is done.

* **Waitable Timer**: The original method that's consistent but slightly inaccurate. This is still the default setting.
* **Sleep**: A different method that may work better but also may cause stuttering on some computers.
* **Busy Wait**: An extremely intensive but effective method.
* **Sleep and Busy Wait**: A combination of the previous 2 that sleeps for most of a frame and then busy waits for the rest.

## Free Roam
Added this new hack that disables all missions and unlocks everything.

## Letterbox
Fixed an issue where movies could display incorrectly if the Movies setting in Aspect Ratio Support was disabled or Aspect Ratio Support itself was disabled.

## Modern Computer Support
Fixed an issue where the frame delta time could be 0 if the FPS went over 1000. This could cause things (like the player's position) to become NaN.

This fix can be disabled with the -allowzerodeltatime command line argument.

## No Neither Road Arrow Processing
Added this new hack. This fixes an issue where the game tries to process road arrows during a "neither" stage which can cause crashes in certain cases.

You probably shouldn't require this unless that comes up but it probably won't in Radical's maps.

## No Saved Games
Added this new hack that entirely disables the loading and use of saved games.