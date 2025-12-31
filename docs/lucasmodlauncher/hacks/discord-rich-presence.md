---
title: Discord Rich Presence
description: "This hack adds Discord Rich Presence to the game."
---

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List.**

This hack adds Discord Rich Presence to the game that shows what main mod, level and mission you're currently playing.

# Settings
## Show Main Mod
Sets whether or not to show the current main mod.

**Defaults to Enabled.**

## Show Mission Elapsed Time
Set whether or not to show the elapsed time of the current mission.

**Defaults to Enabled.**

# Configuring This Hack
To configure this hack from a mod when its enabled, create a file named `DiscordRichPresence.ini` and add the parameters necessary for your mod inside it.

```ini
; [Global] Section: Set the titles for missions on every level.
    ; Currently only supports setting the titles for the Bonus Missions, Street Races and Wager Races.

[Global]
BonusMission=Example Bonus Mission
StreetRace1=Example Street Race 1
StreetRace2=Example Street Race 2
StreetRace3=Example Street Race 3
WagerRace=Example Wager Race
```

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-discord-rich-presence) for the Mod Launcher.

# Version History
## 1.23.10
{{ snippet lucasmodlauncher/versions/1.23.10/hack_discord-rich-presence }}

## 1.23.8

* Added the `-nodiscordrichpresence` command line argument.
* Made the Bonus Mission, Street Race and Wager Race titles configurable by mods.

## 1.23
Updated the description of this hack.

## 1.22

* Added the "RapidJSON" license.
* Made this hack output `DISCORD RICH PRESENCE: Initialising...` when initialising Discord RPC.
* Made this hack wait until the main menu to initialise Discord RPC.
    * This seems to make the hack work far more reliably than before.

## 1.21

* Fixed an oversight where the hack was listed on Windows XP.
* Updated to a newer version of Discord RPC.

## 1.18
Moved this hack to the new "Settings" page.

## 1.16.3
Added this hack.