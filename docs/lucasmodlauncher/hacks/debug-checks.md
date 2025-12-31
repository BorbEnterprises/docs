---
title: Debug Checks
description: "This hack adds various checks and error messages that help with debugging mods."
---

**This is a [developer hack](all-hacks.md#developer-hacks) that can be enabled on the "Developer" page of the Mods List.**

This hack adds various checks and error messages that help with debugging mods.

# Settings
## Missing Detection > Locator
Makes the hack show an error message when a locator is not found.

**Defaults to Enabled.**

**NOTE:** These messages can show up when playing the original game because Radical screwed up in a number of places.

## Missing Detection > Composite Drawable *(Experimental)*
Makes the hack show an error message when a composite drawable is not found.

**Defaults to Enabled.**

## Use Legacy Names
Makes the hack use older, unofficial chunk names.

**Defaults to Disabled.**

## Combine Zone Tree Node Exceeded Messages
Makes the hack combine multiple tree nodes having their limits exceeded into a single message.

**Defaults to Enabled.**

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-debug-checks) for the Mod Launcher.

# Version History
## 1.26
{{ snippet lucasmodlauncher/versions/1.26/hack_debug-checks }}

## 1.25
{{ snippet lucasmodlauncher/versions/1.25/hack_debug-checks }}

## 1.23.11
{{ snippet lucasmodlauncher/versions/1.23.11/hack_debug-checks }}

## 1.23.10
{{ snippet lucasmodlauncher/versions/1.23.10/hack_debug-checks }}

## 1.23.9
{{ snippet lucasmodlauncher/versions/1.23.9/hack_debug-checks }}

## 1.23.6

* Added a null-check of the car to the get position and get move speed functions of vehicle positional sound players with a new assert.
    * In other words, this assert can appear after the game tries and fails to play vehicle sounds.
    * Also added the `-novehiclepositionalsoundplayercarnullcheckasserts` command line argument to suppress the assert and allow the game to try to continue.

## 1.23.4

* Fixed a crash when cancelling a mission or failing a mission and choosing "no" when the player is inside some types of disabled triggers.
* Made it so this hack does not assert if a locator is missing if Missing Locator Detection is enabled in Debug Checks.

## 1.23.3
Fixed a null pointer dereference when using the "MUTE" command line argument (enabled by the included "No Audio" mod) that could cause a crash in some cases (observed on Windows XP).

## 1.18
Moved to the new "Developer" page.

## 1.17
Added this hack.