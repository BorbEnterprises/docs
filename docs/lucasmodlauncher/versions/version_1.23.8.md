---
title: Version 1.23.8
description: "This update was released on October 23rd, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on October 23rd, 2019.**

# Launcher
## Localisation
This version adds a couple new language strings related to improved Lua errors.

A new template language (Template_1.23.8.xml) was published on [this page](../localisation.md) including these new strings at the end of the file.

# Hacks
## Hack Support

* Added `-debugstagechange`. This outputs information to the console when you change stages in a mission.
* Made asserts (when not using `-msvcasserts`) log to the log file (when "Logging" is enabled in the "Console and Logging" hack).
* Made crash/exception messages log to the log file (when "Logging" is enabled in the "Console and Logging" hack).

## Additional Script Functionality

* Made it so this hack actually knows the previous or next stage when starting or ending a stage respectively.
	* In previous versions, the hack just guessed the previous or next stage by subtracting or adding one to the current stage index.
	* The old logic could cause issues in certain cases such as bombbarrel (nuclear waste) stages that can send you back multiple stages.
* Fixed a bug where calling `SetPedsEnabled` alongside `StreetRacePropsLoad` would cause pedestrians to become disabled after the mission ends until another mission puts it back.

## Custom Files

* Made it so the start of Lua file names are truncated instead of the end.
	* Also added `-notruncateluafilenamestart` to opt out of this change.
* Made various improvements to Lua execution errors.
	* They now include the title of the mod that executed the script.
	* They now include a stack trace.
		* Also added `-noluastacktrace` to opt out of this addition.
	* They now get logged to the log files (when "Logging" is enabled in the "Console and Logging" hack).
* Made various improvements to Lua load errors.
	* They now include the title of the mod that loaded the script.
	* They now get logged to the log files (when "Logging" is enabled in the "Console and Logging" hack).

## Custom Text
Added support for defining variables and using them in text strings.

## Discord Rich Presence

* Added the `-nodiscordrichpresence` command line argument.
* Made the Bonus Mission, Street Race and Wager Race titles configurable by mods.