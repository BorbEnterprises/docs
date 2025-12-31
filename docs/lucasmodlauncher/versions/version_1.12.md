---
title: Version 1.12
description: "This update was released on October 30th, 2015."
authors: ["loren","lucasc190"]
---

**This update was released on October 30th, 2015.**

# Launcher

## General

* Fixed a bug where settings were not saved in certain circumstances (such as when unticking mods) when your settings are stored in `Settings.ini`.
* Made the Mod Launcher check for updates on startup.
* Moved the "Game EXE Path" setting off the main window into the advanced tab of "Launcher Settings".

## Main Window

* Made the Resolution combo box on the main window use × instead of x.
* Moved the "Disable All" and "Reload" buttons to the upper right corner of the main window.
* Removed the "Launcher Settings..." and "Open Folder..." buttons and replaced them with an "Open..." button.
* Removed the "Large Icons" tickbox from the main window. 
    * This option can now only be found in the right click menu of the Mods List.

## Mods List

* Added the "Decompilable Only" option to the right click menu.
* Fixed a bug where the "Copy Require Line" right click menu item on frameworks used `RequiredMod` instead of `RequiredFramework`.
* Fixed a bug where the "Compilable Only" right click menu item was available in categories that did not support compilable mods when the category was remembered from the previous time the Mod Launcher was open.
* Made the Mods List refreshable with F5 and Control+R.
* Renamed the "None" sub-category of the "Required Hack" category to "None/Hack Support".

## Launcher Settings

* Added a label to the "Non-mod Hacks" page that says "Hover over a hack for more information."
* Fixed a bug on the "Additional Mods Folders" page where adding a new mods folder with the last one in the list selected, the "Down" button would still be disabled until you selected another folder.
* Made the "Non-mod Hacks" page include more hacks.
    * Also made certain advanced hacks such as Hack Support not visible in this list by default, requiring you to right click and enable them first.
* Updated the description of "Hack Support" on the "Non-mod Hacks" page.

# Mod Features

* Added the `Decompilable` property to the `[Compile]` section that allows users to decompile the mod when it's compiled by right clicking it in the Mods List.
* Added the `MinifyPNGs` property to the `[Compile]` section that defaults to on (the previous behaviour) only when the mod is not decompilable.

# Hacks
## General
Added the "Cheat Mods" category to the following hacks:

* Cheat Keys
* No Traffic
* Repair Car On Reset

## Hack Support
Fixed a bug where a message saying "The game was terminated while Hack Support was initialising." would appear if the game's CD check failed.

## Lua Support
Added this new advanced hack. This hack only contains the code for Lua 5.3.1, allowing for multiple other hacks to utilise it without requiring an entire copy of the library.

## Custom Dialogue Character Codes
Added this new hack. This allows you to define custom dialogue character codes.

## Custom Files
{{ snippet lucasmodlauncher/versions/1.12/hack_custom-files }}

## Cheat Keys
Fixed a bug that prevented the 6 key from working in the Bonus Game.

## Custom Car Shop Support
Added this new hack. This allows mods to specify custom car shop NPC names and conversation names.

## Flippable Cars
Added this hack. This can be used to allow cars to flip over.

## Modern Resolution Support

* Made it respect any resolution specified in `simpsons.ini` when the game is running in a Window.
* Made 1024x768, 1152x864, 1280x1024, and 1600x1200 not listed unless they're supported by your graphics card.

## Multiple Instance Support
Made this hack hidden by default.

## No Automatic Saved Game Load
Added this hack. This can be used to prevent the game from loading your most recent save file at startup.

## No Fast Car Reset
Made this hack hidden by default.

## No Time Limits
Added this hack. This can be used to disable time limits in missions.

## Replayable Bonus Missions
Added this hack. It can be ticked in the mods list however mods must add explicit support for it to their level load/init scripts for the functionality to work properly.