---
title: Replayable Bonus Missions
description: "This hack allows bonus missions to be played more than once."
---

**This hack can be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List.**

This hack allows bonus missions to be played more than once.

By default, the game will require the level to be fully reloaded in order to play it again but mods can change the arguments given to [AddNPCCharacterBonusMission](/hitandrun/scripting/mfk-commands/addnpccharacterbonusmission.md) to make it replayable immediately.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=ReplayableBonusMissions
```

# Version History
## 1.23
Updated the description of this hack.

## 1.18
Moved this hack to the new "Settings" page.

## 1.12
Added this hack.