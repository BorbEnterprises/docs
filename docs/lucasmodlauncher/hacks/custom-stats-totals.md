---
title: Custom Stats Totals
description: "This hack adjusts car and skin reward totals for each level based on the amount defined in the rewards file."
---

**This hack must be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

This hack adjusts car and skin reward totals for each level based on the amount defined in the rewards file. It also automatically disables scrap book menus for specific levels if there's too many cars or skins to avoid crashing the game.

It also allows mods to specify the maximum amount of Levels the mod has.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomStatsTotals
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomStatsTotals.ini` and add the parameters necessary for your mod inside it.

```ini
; [Miscellaneous]
	; Levels: The maximum amount of levels.
		; Defaults to 7.

[Miscellaneous]
Levels=7
```

# Version History
## 1.24
{{ snippet lucasmodlauncher/versions/1.24/hack_custom-stats-totals }}

## 1.16
Made the "Clothes" and "Vehicles" menus get disabled in the scrapbook if there aren't any clothes or vehicles registered respectively.

## 1.6
Added this hack.