---
title: Screenshots
description: "This hack allows you to take screenshots."
---

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List.**

This hack allows you to take screenshots with F12 and screenshots that exclude the HUD with Alt+F12 or Control+F12.

# Configuring This Hack
Mods can provide a custom screenshot sound as a WAV file named `ScreenshotTaken.wav` located in the root folder of the mod.

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-screenshots) for the Mod Launcher.

# Version History
## 1.23

* Made non-ingame messages support language localisation.
* Improved error handling.

## 1.22
Made it so holding the F12 key will no longer rapidly take screenshots. Also added a `-continuousscreenshots` command line argument to undo this.

## 1.19
Added the `-debugscreenshots` command line argument.

## 1.18

* Moved this hack to the new "Settings" page.
* Fixed an issue where the default screenshot sound did not work on Windows XP.
* Fixed this hack failing to take screenshots on Wine or Oracle VM VirtualBox Guest Additions.

## 1.16

* Made it play a sound when taking a screenshot.
    * Customisable by mods.
* Made it flash the screen when taking a screenshot.
* Made Control+F12 take a screenshot that excludes the HUD.

## 1.15
Made this hack into a mod hack instead of it being always enabled. It still defaults to enabled.

## 1.4
Added this hack.