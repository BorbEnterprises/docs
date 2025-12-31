---
title: Resizable Window
description: "This hack makes the game's window resizable and maximisable."
status:
    class: "wip"
---

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List.**

This hack makes the game's window resizable and maximisable.

# Settings
## Start Maximised
Set whether or not the window will start maximized.

**Defaults to Disabled.**

## While Resizing
TODO

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-resizable-window) for the Mod Launcher.

# Version History
## 1.23

* Added the `-nomaintainwindowcentre` command line argument. This prevents this hack from trying to maintain the centre point of the game window when the game resizes it.
* Made the game terminate abruptly with no message or crash dump in the case that an exception occurs in the resizing timer callback (instead of letting Windows swallow the exception and likely cause corruption).
* Made this hack check if the game window is currently maximised instead of checking if the "Start Maximised" setting is ticked before suppressing the changing of the resolution when the game loads its settings.
* Made this hack update the game's unmaximised size and position if the game is maximised when it loads its settings.
* Made this hack force the game window to fit within the working area of the screen it's on when maintaining the window centre when the game resizes its window.
* Made this hack prevent you from resizing the client area of the game below 1 pixel on the width or height.
    * Also added a "-allowzerowindowsize" to opt out of this.
* No longer resizes or repositions the window if the resolution changes when the game is in full screen.
    * This became an issue with Hack Support blocking the game from resetting its Direct3D device redundantly in this version.
* No longer maintains the centre of the window when changing out of full screen.
* No longer handles resizing when the game is in full screen.


## 1.19

* Fixed issues when switching from a resizable window to fullscreen.
* Made the game not change its resolution when loading its settings if the window size is changed before then.
* Made the game maintain its center when changing resolution instead of re-recentering on the screen.
* Made the game continue processing and rendering when a Windows context menu (like you'd get when right clicking the caption of the window) is open.

## 1.18
Moved this hack to the new "Settings" page.

## 1.16.3
Made the game maximisable and added a setting for it to start maximised.

## 1.16
Added this hack.