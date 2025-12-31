---
title: Aspect Ratio Support
description: "This hack makes the game properly support different aspect ratios with various configuration options."
status:
    class: "wip"
---

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List.**

This hack makes the game properly support different aspect ratios with various configuration options.

# Settings
TODO

# Frontend Adjustments
TODO

# Version History
## 1.23.2
Fixed a bug where the aspect ratio was updated (and calculated when "Automatic Aspect Ratio" was enabled) every time it was needed instead of only when the resolution changed.

## 1.23
Made it so this hack can no longer be required by mods.

## 1.21
Changed the default "FOV > Mode" from "Fit" to "Average".

## 1.20.1
Fixed an issue where the "Movie Letterbox Colour" setting let you pick an alpha.

## 1.20
Added the "Movie Letterbox Colour" setting.

## 1.18

* Moved this hack to the new "Settings" page.
* Added a new FOV mode called "Average".
* Fixed an issue that caused the aspect ratio to start off corrupt if the Resizable Window hack's "Start Maximised" setting was enabled.

## 1.16.3

* Added a new setting in the FOV group called "FOV" to set the field of view.
* Fixed an issue where the game would be light blue if it was minimised while loading.
* Replaced the "Adjust Field of View" setting with with a new setting in the FOV group called "Mode". Defaults to Fit. Lock Horizontal is the same as the old setting being disabled while Lock Vertical is the same as when it was enabled.

## 1.16.1
Fixed an issue that caused a rare, seemingly random, crash.

## 1.15.1
Fixed an issue where the background of the credits didn't fully cover the screen in some wider aspect ratios.

## 1.15
Added this hack.