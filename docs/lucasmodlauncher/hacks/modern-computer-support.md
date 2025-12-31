---
title: Modern Computer Support
description: "This hack makes various patches to the game to make it work better on modern computers and operating systems."
---

**This hack is [always enabled](all-hacks.md#always-enabled-hacks) when using the Mod Launcher.**

This hack makes various patches to the game to make it work better on modern computers and operating systems.

# Features
This is a list of fixes that are applied by this hack.

* Fixes slow load times on Windows Vista / Windows Server 2003 or newer.
    * This hack does not do this if [Load Manager Thread Coordination](load-manager-thread-coordination.md) is enabled as it is not necessary.
    * How this is achieved is dependent on whether or not "Limit to Single Core" is enabled on the "Game" tab of [Launcher Settings](../settings.md).
        * If enabled, this is done by making any threads created by the game run on your first processor core.
        * If disabled, this hack will instead change various Sleep calls in the game to be called with a 1 instead of a 0.
	* This fix can be opted out of with the [-noslowfileloadfixes command line argument](../command-line-arguments.md#hack-modern-computer-support_-noslowfileloadfixes).
	* This fix can forced on with the [-forceslowfileloadfixes command line argument](../command-line-arguments.md#hack-modern-computer-support_-forceslowfileloadfixes).
* Makes the game window get centered properly in Windowed mode if your screen resolution is wider than 1600 pixels.
* Makes the game work if it's installed to a drive with the letter `A:` or `B:`.
* Makes DirectSound's maximum sample rate 200,000hz instead of 100,000hz in non-English releases of the game.
    * The original English release already has a maximum of 200,000. This change is just to make it consistent.
* Makes it so the game cannot have a delta time of 0 by skipping any frames that would have resulted in that (which happens when the frame-rate goes over 1000).
    * This fixes issues where positions of various things like the player could become NaN (due to the game dividing by 0).
    * This fix can be opted out of with the [-allowzerodeltatime command line argument](../command-line-arguments.md#hack-modern-computer-support_-allowzerodeltatime).
* Fixes an issue where you cannot bind mouse buttons when using a non-English Windows language.
	* This fix can be opted out of with the [-nononenglishwindowsmousebuttonfix command line argument](../command-line-arguments.md#hack-modern-computer-support_-nononenglishwindowsmousebuttonfix).
* Fixes an issue where the game incorrectly centered the cursor to the window instead of it's client area *and* an issue where the game assumed the non-client area was 30 pixels at the top and 10 pixels at the other edges when clipping the cursor.
	* Also added the `-noproperclientareacursorcentringandclipping` command line argument to opt out of this fix.

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-modern-computer-support) for the Mod Launcher.

# Version History
## 1.26.1
{{ snippet lucasmodlauncher/versions/1.26.1/hack_modern-computer-support }}

## 1.26
{{ snippet lucasmodlauncher/versions/1.26/hack_modern-computer-support }}

## 1.25
{{ snippet lucasmodlauncher/versions/1.25/hack_modern-computer-support }}

## 1.21
Fixed an issue where the frame delta time could be 0 if the FPS went over 1000. This could cause things (like the player's position) to become NaN.

## 1.19
Fixed an issue in the game where the border was not removed when in fullscreen (particularly noticable on Windows 10).

## 1.18.3
Now outputs the detected OS version to the [Console](console-and-logging.md) on startup.

## 1.18
Made non-english versions of the game use 200,000hz as the maximum sample rate like the Release English version instead of 100,000hz.

## 1.17.2
Made the game support running from the `A:` and `B:` drives.

## 1.2 or earlier
Added this hack.