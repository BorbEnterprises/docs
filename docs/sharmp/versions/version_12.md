---
title: Version 12
description: "This update was released on July 2nd, 2018."
---

**This update was released on July 2nd, 2018.**

# Launcher
## General
Now based on [Lucas' Simpsons Hit & Run Mod Launcher 1.18](../../lucasmodlauncher/versions/version_1.18.md).

## Settings

* Added "Low Bandwidth" to the Server tab. This makes the client communicate with the server using the old tick-rate of 10.
* Added "Play Offline" to the Server tab. This makes it so you can play by yourself without being connected to the server.
    * This is useful for testing secret stuff and multiplayer checks in your mod without having to use the actual server to do so.

# Mods
## Multiplayer Resources

* Now includes "npd.cho" and "npd_a.p3d" from Multiplayer Cars and Characters so every character has proper animations.

# Hacks
## Debug Text
### RakNet Page

* Added "Actual bytes per second" which shows the combined total of "Actual bytes per second sent" and "Actual bytes per second received".
* Added "Total bytes" which shows the combined total "Total bytes sent" and "Total bytes received".
* Changed it so totals update continuously instead of every second.
* Changed the formatting of bytes. They now shows in KB, MB, etc.

### resync Page
Added this page.

## Multiplayer

* Changed it so the R key no longer deletes the mission icon on the HUD map. This also means the R key used to cycle debug pages in Debug Text is now re-enabled.
* Improved synchronization of car rotations.
* Improved synchronization of entering and exiting vehicles.