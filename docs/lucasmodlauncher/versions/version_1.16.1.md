---
title: Version 1.16.1
description: "This update was released on October 28th, 2017."
authors: ["loren","lucasc190"]
---

**This update was released on October 28th, 2017.**

# Launcher
## Account Integration
Added Donut Team Account Integration.

# Hacks
## Aspect Ratio Support
Fixed an issue that caused a rare, seemingly random, crash.

## Custom Limits

* Added the `DeletedEntityLimit` property to the `[Miscellaneous]` section.
* Added the `PathLimit` property to the `[Miscellaneous]` section.
* Fixed an issue where changing the Intersection limit to higher than normal did not change the amount of animated arrows that got created.
    * This caused crashes since there's supposed to be an instance of the arrows created for every intersection.

## HUD Map Ignore Player Height
Added this new hack. This makes it so the camera for the HUD map ignores the Y position of the player.

## Unlock All Missions
Made this hack do nothing in the Demo version of the game.