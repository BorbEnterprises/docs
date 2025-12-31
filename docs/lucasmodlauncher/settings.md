---
title: Settings
description: "This page documents the Mod Launcher's various settings."
---

This page documents the Mod Launcher's various settings.

# Storing Settings
By default, the Mod Launcher stores its settings in the Windows Registry at the path `HKEY_CURRENT_USER\Software\Lucas Stuff\Lucas' Simpsons Hit & Run Tools\Lucas' Simpsons Hit & Run Mod Launcher`.

You can also make them get stored elsewhere by creating a file named `Settings.ini` next to the Mod Launcher's executable *or* in "Documents\My Games\Lucas' Simpsons Hit & Run Mod Launcher".

# Additional Mods Tab

This tab has options for adding additional Mods Folders as well as Individual Mods to your Mods List from custom locations on your computer.

## Mods Folders
This tab allows you to add additional folders that the mod launcher will search for mods when loading mods.

You can use the "Up" and "Down" buttons on the right side with a folder selected in the list to change the order it's loaded in.

The "Disable" checkbox can also be used to disable a selected folder without outright removing it.

## Individual Mods
This tab will allow you to add individual mod folders or files to your mods list.

The "Disable" checkbox can also be used to disable a selected mod without outright removing it.

# Game Tab

## Game EXE Path
This is the path to your installation of The Simpsons Hit & Run.

This needs to be set for the launcher to able to launch the game.

## Crashes
### Save Crash Dump
This makes the Mod Launcher save a crash dump when the game crashes that can sometimes be useful for debugging if submitted to us.

The Crashes folder can be found with "Open > Crashes..." on the bottom left of the main window.

**Defaults to Enabled.**

### Terminate on Crash
This makes the Mod Launcher terminate the game immediately if it crashes.

It is recommended you do not enable this feature.

**Defaults to Disabled.**

### Show Message on Crash
This makes the Mod Launcher show a message when the game crashes containing the memory address where the crash occurred.
   
This is helpful for Windows 10 users running the April 2018 Update or later since Microsoft removed the program crash message altogether and as a result made it harder to find out where the game crashed.

**Defaults to Disabled.**

## Advanced 
### Always Keep Saved Games Separate
This makes the Mod Launcher use a separate saves folder from the vanilla game even when no Main Mod is enabled. 

The general Saved Games folder can be found with "Open > Saved Games..." when there is no Main mod enabled.

**Defaults to Disabled.**

### Keep Settings Separate
This makes the Mod Launcher tell the game to load its `simpsons.ini` settings file from the Mod Launcher's folder in your Documents instead of the game's install directory.

**Defaults to Disabled.**

### DPI Aware
This makes the game support different DPI displays on Windows 7 or newer.

**Defaults to Enabled.**

### Visual Styles
This makes messages shown by the game and hacks support Windows visual styles.

**Defaults to Enabled.**

### Start in Correct Resolution
This makes the game start in the correct resolution instead of briefly being in 800x600 before switching to the user's resolution.

**Defaults to Enabled.**

### Limit to Single Core
This limits the game to a single processor core.

**Defaults to Disabled.**

# Launcher Tab
## Language
This allows you to choose a language for the Mod Launcher to use on it's interface and in certain hacks.

This setting is only displayed if there are additional languages present in a Languages folder next to the Mod Launcher's executable.

**Defaults to English.**

## Check for Updates
This allows you to set whether or not the Mod Launcher will communicate with the Donut Team website to check for updates.

**Defaults to Enabled.**

## Donut Team Account Integration Support
This setting allows you to fully toggle Donut Team Account Integration without signing out.

**Defaults to Enabled.**

## Close to Tray
This makes the Mod Launcher close to a tray icon instead of exiting.

**Defaults to Disabled.**

## DPI Aware
This makes the Mod Launcher support different DPI displays on Windows 7 or newer.

**Defaults to Enabled.**

# Non-mod Hacks Tab
This tab contains a list of loaded hacks that are not Mod Hacks.

# Licenses Tab
This tab contains various licenses for libraries used by the Mod Launcher itself and any loaded hacks.