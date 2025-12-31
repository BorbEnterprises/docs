---
title: Version 1.19
description: "This update was released on October 2nd, 2018."
authors: ["loren","lucasc190"]
---

**This update was released on October 2nd, 2018.**

# Banner
![version 1.19 release banner](/img/lucasmodlauncher/version-banners/1.19.png)

# Highlights

* **Additional Script Functionality**: Vehicle Character Commands
* Language Localization Support for the Mod Launcher's Interface
    * The Mod Launcher still only ships with English.
* Lens Flare Hack
* Video Texture Support Hack

# Launcher
## General

* Added "dbghelp.dll" to the DLLs folder. This is used to save crash dumps.
* Added the `-debugloadhacks` command line argument.
* Added the `-loadhackspause` command line argument.
* Fixed a crash when using "-launch" with "Start in Correct Resolution" enabled (as is the default).
* Made the game only start in the correct width and height when starting windowed.
* Made the Mod Launcher restart if the shift key is held down when reloading all mods.
* Made the unhandled exception message have an error icon instead of no icon.
* Removed limitations on how many mods, hacks and mod settings could be injected into the game.
    * You don't want to know.

## Main Window
Made the main window re-centre to the screen the loading window was moved to if it was moved to another screen while reloading.
Made the main window start on the screen the loading window was last on.
Made the error message shown when failing to load mods show after the main window.
Made the loading window appear on the screen the main window was on when reloading.

## Mod Info
Made "Size" on the Advanced tab of the Mod information panel available when using -noscanmodfiles for hacks and compiled mods.

## Mod Settings
Fixed an issue where the icon of the Mod Settings window when using "-settings" where the default .NET icon instead of the Mod Launcher's Icon.

## Launcher Settings
Added "Limit to Single Core" to the "Game" tab.

## Localisation
Added support for Language Localization.

# Hacks
## Additional Script Functionality
This update brings about the ability to add characters to the player's car or stage vehicles.

You can use this exciting new functionality to have passengers accompany the player in missions and just have characters present in a car.

### CON Commands

* Added the `AddVehicleCharacter` command.
* Added the `SetVehicleCharacterAnimation` command.
* Added the `SetVehicleCharacterJumpOut` command.
* Added the `SetVehicleCharacterScale` command.
* Added the `SetVehicleCharacterSuppressionCharacter` command.
* Added the `SetVehicleCharacterVisible` command.

### MFK Commands

* Added the `AddStageVehicleCharacter` command.
* Added the `RemoveStageVehicleCharacter` command.
* Added the `SetStageVehicleCharacterAnimation` command.
* Added the `SetStageVehicleCharacterJumpOut` command.
* Added the `SetStageVehicleCharacterScale` command.
* Added the `SetStageVehicleCharacterVisible` command.
* Added the `SetStageVehicleAllowSeatSlide` command.
* Updated `SetStageCharacterModel` to default the second argument to the player's current animation set instead of requiring the argument.

## Bug Fixes

* Added "Actors" > "Restore Wasp Collision".
    * This fixes an issue where destroying a certain number of wasps disables their collision until the level is fully reloaded.
* Changed the tooltip for "Character Rotations" to be more specific about what it does. The hack's description was also updated to reflect this change.
* Made "Fix Steering Animations" also fix the steering/swaying animation cancelling immediately/starting again repeatedly.

## Custom Audio Format Support
Added support for Lua Path Handler Redirections on RSD files to FLAC and Ogg files.

## Custom Files
### General

* Made CustomFiles.lua execute after all hacks that are supposed to be loaded are loaded.
* Made this hack only mount "CustomFiles" folders that exist.
    * This change can dramatically improve performance if you have lots of mods enabled but only a few have CustomFiles folders (like Mod Hacks for instance).

### Lua Scripting

* Added `GetLauncherVersion`. This returns the current version of the Mod Launcher.
* Added `GetMainMod`. This returns the InternalName of the current main mod (if there is one).
* Added `GetSettings`. This returns the settings of the current mod (or the specified mod) in a Lua table.
* Added `IsTesting`. This checks if the user is has the Mod Launcher's testing mode enabled.
* Added `UseCallbacks`. This is an advanced function for handling files with Lua that may or may not have a use case.
* Fixed an issue where "ComparePaths" was always case sensitive and always slash sensitive.

## Debug Text
### General

* Made Ctrl+C copy the current page text to clipboard.
    * Also added "Allow Copying with Ctrl+C" to the "Advanced" tab of the hacks settings to disable that.

### "actors" Page
Added this page.

### "cams" Page
Made this page exclude null cameras.

### "characters" Paege
Added this page.

### "intersects" Page
Made this page not say "Y: " before the Y and "Z: " before the Z of "Intersect triangle pos 3".

### "loaded characters" Page
Added this page.

### "missions" Page
Made this page exclude null missions.

### "mission" Page

* Made this page show "null" for null objectives instead of crashing.
    * This is helpful for debugging in the event the stage's objective is not getting added.

### "traffic" Page
Made this page render the segments of the road the car is currently on (and the previous roads segments if the car is on an intersection).

### "triggers" Page

* Made this page include the type number of locators in brackets after the type name.
* Made sphere triggers render as spheres now instead of boxes.

## Debug Test
### General
Removed the F9 dialog to list all entered triggers.

### Menus Page
Made "Main Menu" > "No Glow Hide" work in the demo version of the game even though this version skips the Main Menu entirely.

### Graphics Page

* Added "No Texture/Alpha Operations/Arguments".
* Added "PDDI Windowed".
* Added "No Force Back-faces".
* Removed "Lens Flare".

### Speedometer Page
Made "Use Miles Per Hour" and "Show Units" work in the demo version of the game.

### Vehicles Page

* Added "Lisa Y Offset".
* Made "Target Player" work in game versions other than Release English.

### Sky Page
Made "Scale" and "Position" work in game versions other than Release English.

### Miscellaneous Page

* Made "Cursor" > "Show Windows Cursor" work in game versions other than Release English.
* Made "No Splash Screen Loading" work in the demo version.

## Interprocess Communication
Fixed an issue where the Pure3D Editor would hang when selecting locators or right clicking on 3D views in some cases with the following changes:

* Made this hack still respond if the game is in a blocking modal loop or minimized while in fullscreen mode..
* Made this hack uninitialise if the game crashes.

## Modern Computer Support
Fixed an issue in the game where the border was not removed when in fullscreen (particularly noticable on Windows 10).

## Lens Flare
Added this new hack. This makes Lens Flares work just like the console releases of the game.

## Resizable Window

* Fixed issues when switching from a resizable window to fullscreen.
* Made the game not change its resolution when loading its settings if the window size is changed before then.
* Made the game maintain its center when changing resolution instead of re-recentering on the screen.
* Made the game continue processing and rendering when a Windows context menu (like you'd get when right clicking the caption of the window) is open.

## Screenshots
Added the `-debugscreenshots` command line argument.


## Video Texture Support
Added this new hack. This allows you to use BIK files as textures.