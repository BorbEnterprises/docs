---
title: Debug Test
description: "This hack contains various experimental features."
status:
    class: "wip"
---

**This is a [developer hack](all-hacks.md#developer-hacks) that can be enabled on the "Developer" page of the Mods List.**

This hack contains various experimental features.

# Settings
TODO

# Other Features
TODO

# Version History
## 1.23.10
{{ snippet lucasmodlauncher/versions/1.23.10/hack_debug-test }}

## 1.23.1
Fixed a [conflict](/img/lucasmodlauncher/misc/asf_debugtest_conflict.png) between Additional Script Functionality and Debug Test when the "Menus > Pause Menu > Pause Always Allowed" setting was enabled.

## 1.23
Made non-ingame messages support language localisation.

## 1.22
### General

* Made it only check if the "H" key is down once each frame instead of once for every possible collision.
* Made it only check if the "H" key is down when the game window is focused.
* Made the vehicle controller used when possessing vehicles with the 8 key only get the key states once each frame.
    * Did you know about this feature? We didn't.
* Made possessing vehicles with the 8 key still use their old controller when not accelerating or steering, not switch them to in-car physics until accelerating or steering and take traffic cars off rails when not accelerating or steering.
    * No seriously, Lucas found out he did this recently. I wonder what other secrets there are...
    * Loren should really document Debug Test sometime.

### Graphics Page

* Added "Software Vertex Processing".
* Added "Flip > X", "Flip > Y", "Flip > Z" and "Flip > Cull Mode" to flip the viewport in wacky ways.

### Vehicles Page

* Added "Air Vent Force". Now your car can soar like a candy wrapper in an updraft.
    * This suppresses the new "Vehicles > No Air Vent Audio" feature of Bug Fixes if the force is not 0.
* Added "Override Maximum Traffic".
* Added "No Load Properties" to disable the game loading CON files.
    * Also added "Set Up Vehicle Handling" and "Create Driver" to make the game do some initialization stuff it would've done if it loaded the CON file.
* Removed the limit of 5 on "Vehicles > Road Nodes > Maximum Cars".

### Miscellaneous Page

* Added "Gravity" settings. Far out!
    * Screen might go blue if you set some of these numbers the wrong way. No warranty included.
* Added "Heaps > No Temp Heap".
* Moved "Use Tracking Heaps" into the new "Heaps" group.

## 1.21
### Graphics Page
Removed "Anti-aliasing".

### Vehicles Page
Fixed an issue where "Target Player > Traffic" did not work in the Best Sellers Series version of the game.

### Miscellaneous Page
Fixed a mistake where "Delta Time" was mislabeled to as "Substeps" (a different concept).

## 1.20
### General
Renamed the "Sky" page to "World Spheres".

### Menus Page
Removed "No Camera Animations" in the "Main Menu" section.

### World Spheres Page
Added "Activate Dynamic World Spheres" as a setting instead of forcing it when this hack was enabled.

### Miscellaneous Page

* Removed "Allow Cancel Initial Walk".
* Removed "No Go To Objective Camera Focus".

## 1.19
### General
Removed the F9 dialog to list all entered triggers.

### Menus Page
Made "Main Menu" > "No Glow Hide" work in the demo version of the game even though this version skips the Main Menu entirely.

### Graphics Page

* Added "No Texture/Alpha Operations/Arguments".
* Added "PDDI Windowed".
* Added "No Force Back-faces".
* Removed "Lens Flare".

### Speedometer Page
Made "Use Miles Per Hour" and "Show Units" work in the demo version of the game.

### Vehicles Page

* Added "Lisa Y Offset".
* Made "Target Player" work in game versions other than Release English.

### Sky Page
Made "Scale" and "Position" work in game versions other than Release English.

### Miscellaneous Page

* Made "Cursor" > "Show Windows Cursor" work in game versions other than Release English.
* Made "No Splash Screen Loading" work in the demo version.

## 1.18
### General
Moved to the new "Developer" page.

### Menus Page

* Removed "Force Mission Select Level Reload".
* Removed "No Cursor Until Mouse Move".

### Graphics Page
Added "Default Resolution". This allows you to configure the default resolution of the game window before the game loads your settings.

### Debug Page
* Removed "Ignore Suppressed Drivers".
* Removed "Starting Coins".

### Vehicles Page
Added "No Destroyed Car Jump Out".

### Audio Page

* Added "Force Level RMS". This setting allows you to force a specific level's RMS file to always be loaded/used.
* Added "No Pause Audio Fade".

### Miscellaneous Page

* Added "Disable Window Ghosting".
* Added "No Handle File Not Found".
* Added "Use Camera Position".
* Added "No Animated Camera Letterbox".
* Added "Use Tracking Heaps".
* Removed "No Suppressed Drivers" (yes, there were two of these settings).

### Other

* Made the K Key reload the music RMS file and trigger an event named "Test" if it exists.
* Made Shift+F10 fail the first condition of the active stage (if the stage has any conditions).

## 1.17.2

* Added "No Cursor Until Mouse Move" in the Menus tab.
* Added "No Suppressed Drivers" in the Miscellaneous tab.

## 1.17
Added this hack.