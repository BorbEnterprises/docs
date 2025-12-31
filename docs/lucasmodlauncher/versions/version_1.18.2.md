---
title: Version 1.18.2
description: "This update was released on July 8th, 2018."
authors: ["loren","lucasc190"]
---

**This update was released on July 8th, 2018.**

# Launcher
## General

* Fixed an issue where the Mod Launcher update dialog could appear while loading mods.
* Fixed an issue where the Mod Launcher update dialog could appear over the account window.
* Fixed an issue where cancelling the Launcher Settings dialog would prevent the Mod Launcher update dialog from appearing.

# Hacks
## 3D Phone Booth Preview Support
Made the game assert when loading if `Phonebooth.pag` in "art\frontend\scrooby\ingame.p3d" is missing the `PreviewWindow`, `RewardFG` or `RewardBG` frontend elements required for the hack to work.

## Bug Fixes
Fixed an issue where `BugFixes.ini` wasn't required and wasn't included when compiling mods that require the hack.

## Custom Interior Support
Fixed a crash on startup that occurred with certain game executables.

## Custom Shop Support
Fixed a crash on startup that occurred with certain game executables in certain circumstances:

* If the mod used the `Locator` attribute on a `Selector` element inside a `PhoneBooth` element.
* If the mod used a `Car` element inside a `FreeItems` element inside a `PhoneBooth` element.

## Debug Text
### "states and actions" Page

* Added " (no wait)" after actions that their set does not wait for.
* Added "Walker locomotion action time", "Walker locomotive action next idle animation time" and "Walker locomotive action can play idle animation"

### "lights" page
Removed "enabled" for lights and made disabled lights instead show " (disabled)" after them.

## Debug Test
### Miscellaneous Page
Added "No First Stage Repeat".