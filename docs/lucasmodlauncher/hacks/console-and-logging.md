---
title: Console and Logging
description: "This hack adds a console and support for log files window that the game, mods and hacks can output to."
---

**This is a [developer hack](all-hacks.md#developer-hacks) that can be enabled on the "Developer" page of the Mods List.**

This hack adds a console and support for log files window that the game, mods and hacks can output to.

# Settings
## Console
### Enabled
Set whether or not the console window enabled.

**Defaults to Enabled.**

### Pause on Exit
Set whether or not the console will pause and say "Press any key to continue..." when the game exits.

**Defaults to Disabled.**

### Include Timestamps
Set whether or not to include timestamps before each thing that is outputted to the console.

**Defaults to Disabled.**

## Logging
### Enabled
Set whether or not logging is enabled.

**Defaults to Disabled.**

### Mode
Set if the hack will log to a single `Log.txt` or a `Logs` folder.

* **Log.txt**: The hack will log to a single file, overwriting it each time (unless **Append** is also enabled).
* **Logs Folder**: The hack will create logs in a folder, creating a new one each time you start the game.

**Defaults to Log.txt.**

### Append
Set if the hack will append new logs to **Log.txt** instead of overwriting it when in that mode.

**Defaults to Disabled.**

### Include Timestamps
Set whether or not to include timestamps before each thing that is logged.

**Defaults to Enabled.**

## Include
### Game
Sets whether or not the games outputs will be shown in the console.

**Defaults to Disabled.**

### Mods
Sets whether or not mod output will be shown in the console.

**Defaults to Enabled.**

### Hacks
Sets whether or not hack output will be shown in the console.

## Include Categories
Sets whether or not to include categories (`[GAME]`, `[MOD]` or `[HACK]`) before each thing that is outputted to the console and logged to the log file.

**Defaults to Disabled.**

**Defaults to Disabled.**

# Version History
## 1.23.6

* Made it so the hack will create multiple logs if its unable to write to the log file instead of showing an error message and not logging.
    * In these cases, the hack will just stick a number on the end of the file name like `Log (2).txt`.
* Fixed a crash when failing to open the log file with "Append" ticked.
* Fixed a crash when suppressing RCF files and asyncronous file load requests using Custom Files with this hack enabled and "Include > Hacks" ticked.

## 1.23.5

* Added settings to include Timestamps in the console and/or in log files.
* Added a setting to include categories (`[GAME]`, `[MOD]` or `[HACK]`) in the console and log files.

## 1.23.3

* Added support for logging to a file.
    * Also renamed this hack to "Console and Logging" and updated its description to coincide with this addition.
* Made whether or not the console is enabled based on a setting inside the hack instead of whether or not the hack is enabled.
    * Defaults to enabled.
    * This is also to coincide with the new logging feature as they can be enabled independently of one another.
* Made it so this hack hooks the output function used by libpng so it can be affected by the "Include > Game" setting and included in logs.

## 1.22
Made the title of the console window "Lucas' Simpsons Hit & Run Mod Launcher Console" instead of the path to the game.

## 1.18
Moved this hack to the new "Developer" page.

## 1.9
Added this hack.