---
title: Version 1.18.3
description: "This update was released on July 12th, 2018."
authors: ["loren","lucasc190"]
---

**This update was released on July 12th, 2018.**

# Launcher
## General

* Added a sprinkle of unspeakable evil to mitigate the game hanging on exit in certain cases.
* Fixed an issue where the Mod Launcher update dialog could appear over Mod Settings windows.

## Launcher Settings

* Added a "Start in Correct Resolution" setting on the "Game" tab. Defaults to enabled.

# Mod Features
Fixed an issue where "3DPhoneBoothPreviewSupport.ini" wasn't included when compiling mods.

# Hacks
## Debug Test
### Graphics Page
Removed "Default Resolution". This is now done automatically as mentioned above.

## Debug Text
### General
Made the in-world text of the "triggers", "character joints", "car joints", "dyna phys", "static phys", "road segments" and "car matrix" pages render under the frontend.

### "fences" Page
Added this page. This page renders Fence collision in the world.

### "intersect" Page

* Added "Tree node min" and "Tree node max".
* Added "Tree node parent offset".
* Changed "Intersect normal" to "Intersect triangle normal".
* Now renders the current intersect on top of the world.
* Now shows the memory location of the current Intersect.
* Now shows the vertex positions of the current Intersect triangle.

### "paths" Page
Added this page. This page renders pedestrian Paths on top of the world.

"tree" Page
Now renders the bounding box of the tree node and renders all of the intersects inside it.

## Modern Computer Support
Now outputs the detected OS version to the Console on startup.