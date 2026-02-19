---
title: "Version 1.13.2"
description: "Changelog for Version 1.13.2 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on June 6, 2016.**

# Launcher
## General
* Fixed issues on systems where the decimal symbol is not a "."
* Made the Mod Launcher ignore the compatibility mode setting of Simpsons.exe when "Modern Computer Support" is enabled (which it always is by default).
* Fixed a bug where `CustomDialogueCharacterCodes.ini` wasn't included when compiling a mod.
* Fixed a bug where `CustomMissionSkipFailCounts.ini` wasn't included when compiling a mod.

# Mods List
* Fixed a bug introduced in Version 1.13 where non 7-bit ASCII characters were displayed as question marks in the mod information panel.
* Fixed a crash when changing non-integer number settings.
* Made it so mods that default to being enabled such as Frame Limiter will now become enabled again when using the "Disable All" button.

# Updated Hacks
## Custom Files
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13.2/Hacks/CustomFiles.md }}