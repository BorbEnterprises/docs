---
title: Frame Limiter
description: "This hack limits the frame rate of the game to an amount specified in the hack's settings with additional options to configure when and how this is done."
status:
    class: "wip"
---

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List.**

This hack limits the frame rate of the game to an amount specified in the hack's settings with additional options to configure when and how this is done.

# Settings
## Target Frame Rate
The frame rate that the hack will attempt to reach with the selected Method (see below for more details).

**Defaults to 60.**

## Limit While on Loading Screens
Set whether or not the frame rate will be limited on loading screens.

**Defaults to Disabled because this is because this negatively impacts loading times.** <!-- TODO: Probably not when Load Files while waiting is on? Ask Lucas. -->

## Limit While on Menus
Set whether or not the frame rate will be limited on the main menu and the pause menu.

**Defaults to Enabled.**

## Method
### Waitable Timer
TODO

**This is the default method.**

### Sleep
TODO

### Busy Wait
TODO

### Sleep and Busy Wait
TODO

## Compensation Limit (ms)
TODO

## Load Files While Waiting
This makes it so files can be loaded while the game is waiting for the next frame. [Load Manager Thread Coordination](load-manager-thread-coordination.md) is used to achieve this.

**Defaults to Disabled.**

# Version History
## 1.23.9
{{ snippet lucasmodlauncher/versions/1.23.9/hack_frame-limiter }}

## 1.23.2
Added the experimental "Load Files While Waiting" setting. This makes it so files can be loaded while the game is waiting for the next frame.

## 1.23
Updated the description of this hack.

## 1.22
Made the loading screen used when returning to the main menu or going to the Bonus Game menu from the main menu uncapped when "Limit > While on Loading Screens" is disabled but not when "Limit > While on Menus" is disabled.

## 1.21
Added a new "Method" setting for controlling how the frame limiting is done.

## 1.18
Moved this hack to the new "Settings" page.

## 1.13
Made this hack default to being ticked as the game has issues of varying severity at frame rates above or below a certain range (the game runs best at 60 FPS).

## 1.10
Added this hack.