---
title: Version 1.13.2
description: "This update was released on June 6th, 2016."
authors: ["loren","lucasc190"]
---

**This update was released on June 6th, 2016.**

# Launcher

## General

* Fixed issues on systems where the decimal symbol is not a "."
* Made the Mod Launcher ignore the compatibility mode setting of `Simpsons.exe` when "Modern Computer Support" is enabled (which it always is by default).

## Mods List

* Fixed a bug introduced in Version 1.13 where non 7-bit ASCII characters were displayed as question marks in the mod information panel.
* Fixed a crash when changing non-integer number settings.
* Made it so mods that default to being enabled such as Frame Limiter will now become enabled again when using the "Disable All" button.

# Mod Features

* Fixed a bug where `CustomDialogueCharacterCodes.ini` wasn't included when compiling a mod.
* Fixed a bug where `CustomMissionSkipFailCounts.ini` wasn't included when compiling a mod.

# Hacks
## Custom Files
Fixed a crash when redirecting files loaded by frontend pages.