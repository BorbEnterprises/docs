---
title: "Discord Rich Presence"
description: "This hack adds Discord Rich Presence to the game."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 375 # 1.16.3
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

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
This hack is affected by certain [[../CommandLineArguments.md]] for the Mod Launcher.

# Version History
## Version 1.23.10
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/DiscordRichPresence.md }}

## Version 1.23.8
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.8/Hacks/DiscordRichPresence.md }}

## Version 1.23
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23/Hacks/DiscordRichPresence.md }}

## Version 1.22
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/DiscordRichPresence.md }}

## Version 1.21
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.21/Hacks/DiscordRichPresence.md }}

## Version 1.18
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18/Hacks/DiscordRichPresence.md }}