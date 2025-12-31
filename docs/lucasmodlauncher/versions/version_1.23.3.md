---
title: Version 1.23.3
description: "This update was released on August 16th, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on August 16th, 2019.**

# Launcher
## Localisation
This version adds a couple new language strings related to updates for the "Console" hack.

A new template language (Template_1.23.3.xml) was published on [this page](../localisation.md) including these new strings at the end of the file.

# Mod Features
Increased the maximum length of the `Name` property of `[Setting]` sections from 63 to 127 characters.

# Hacks
## Bug Fixes
Added "Physics > Baby Van Tilt". This fixes a famous bug that most notably causes the baby van in Level 5 Mission 3 to be tilted and have incorrect physics. 

This bug as well as this fix both apply to other cars as well though it appears most prominently on this one so it's named after it.

We also added a `FixUninitialisedArticulatedPhysicsObjectCloneRelativeCentreOfMassAndInertiaMatrixUpdateInterval` property to the `[Physics]` section of BugFixes.ini so mods can opt into this bug fix. The name is very literal.

This bug fix exists as a result of extensive research done by [aldelaro5](https://twitter.com/aldelaro5). He also made an in depth video explaining the bug which can be found [here](https://www.youtube.com/watch?v=u5J8hZgTuW4) if you're interested.

## Console

* Added support for logging to a file.
    * Also renamed this hack to "Console and Logging" and updated its description to coincide with this addition.
* Made whether or not the console is enabled based on a setting inside the hack instead of whether or not the hack is enabled.
    * Defaults to enabled.
    * This is also to conincide with the new logging feature as they can be enabled independently of one another.
* Made it so this hack now controls console output from libpng so it can be affected by the "Include > Game" setting and included in logs.

## Debug Checks
Fixed a null pointer deference when using the "MUTE" command line argument (enabled by the included "No Audio" mod) that could cause a crash in some cases (observed on Windows XP).

## Debug Text
### "AI cars" Page
Added this page.

### "car physics objects" Page
Added this page.

### "fences" Page
Fixed an issue introduced in 1.23.2 where switching to this page made the game render one-sided faces as two-sided.

## Frame Limiter
Fixed an issue where mission loading screens (used when selecting a mission or starting one) were considered menus instead of loading screens.