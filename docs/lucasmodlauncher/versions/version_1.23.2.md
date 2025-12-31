---
title: Version 1.23.2
description: "This update was released on July 29th, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on July 29th, 2019.**

# Launcher
## General

* Made it so Windows messages about the game process failing to start will get shown (such as when a DLL is missing).
* Made it so the message from the `-debuglaunch` command line argument will no longer show up a second time if mods or hacks change in such a way that the Mod Launcher reloads all mods and hacks before starting the game.

## Mods List

* Fixed an issue where mods that were enabled by default and then disabled by the user would become enabled again when unticking "Defaults" for the configuration *or* when they're no longer enabled by default (which can happen when they're updated).
* Fixed an issue where mods that were hidden by default then unhidden by the user would become hidden again when they're no longer set to be hidden by default (which can happen when they're updated).
* Made it so ticking a mod that conflicts with multiple enabled mods will show a message for each conflicting mod.
* Made it so the `-nounreleased` command line argument doesn't prevent the warning message shown when compiling mods that are marked as unreleased.

## Mod Settings
Fixed an issue where these windows allowed enough space for the widest label next to the widest input control even if they were in different groups.

## Localisation
This version adds a few new language strings.

A new template language (Template_1.23.2.xml) was published on [this page](../localisation.md) including these new strings at the end of the file.

# Mod Features

* Added the `PublicTesting` property to the `[Miscellaneous]` section. This is intended for mods that are public but are not a proper release.
    * Currently, this property is exactly the same as `Unreleased` except there will not be a warning when compiling the mod with this property enabled.
    * This property overrides `Unreleased` if they're both enabled. This allows mods that target older Mod Launcher versions to be backwards compatibile by enabling both.
* Made it so the `CommandLine` property in the `[Miscellaneous]` section can be repeated to specify command line arguments for the game on multiple lines.

# Mods
Added the No Audio mod.

# Hacks
## Hack Support

* Fixed a bug introduced in Version 1.23 where hacks were not notified when the Direct3D device was lost. 
    * This caused a crash when resetting the device (such as when changing the game's resolution) while saving screenshots or after the Lens Flare had been on screen.
        * There may have also been other crashes as a result of this issue.
* Made the crash message include " (C++ exception)" or " (integer division by zero)" after the code if it's one of those types of exceptions.
    * If it's a C++ exception, it also shows the [type name](https://docs.microsoft.com/en-us/cpp/cpp/type-info-class?view=vs-2017), value (if it's a long integer) and the result of [what](https://en.cppreference.com/w/cpp/error/exception/what) (if it's an `std::exception`).
* Made using the `-breakgame` and `-suspend` command line arguments together cause the message from `-suspend` to get shown by the Mod Launcher before resuming the injection thread (instead of being shown from inside the game process).
    * This also prevents the breakpoint from `-breakgame` from happening if there's a debugger attached to the game.

## Aspect Ratio Support
Fixed a bug where the aspect ratio was updated (and calculated when "Automatic Aspect Ratio" was enabled) every time it was needed instead of only when the resolution changed.

## Custom Controller Support

* Fixed a bug where Rumble did not work properly (which affects controllers when using the XInput hack since it uses this hack).
* Made connecting a controller flag its output values as having changed (causing the XInput hack to call [XInputSetState](https://docs.microsoft.com/en-us/windows/win32/api/xinput/nf-xinput-xinputsetstate)).

## Debug Text
### General

* Added a "keyboards" page, a "mice" page and a "steering wheels" page to a new "controllers" group.
* Moved the "gamepads" page to the new "controllers" group.

### "fences" Page
Fixed a bug where this page didn't set the cull mode before rendering the fences (causing the fences to only be visible from one side in some cases).

### "mission" Page
Fixed a crash when a stage condition is null (which will crash the game when reaching the stage).

### "music" Page
Fixed a crash when using the game's "MUTE" command line argument (which is enabled by the new No Audio mod).

## Direct3D 9

* Made this hack requirable by other hacks.
* Made unimplemented functions show a message saying they're not implemented with the the name (signature) of the function. These messages have an OK button to attempt to continue as well as a Close button to terminate the game.
    * This is instead of the generic assert they showed before.

## Frame Limiter
Added the experimental "Load Files While Waiting" setting. This makes it so files can be loaded while the game is waiting for the next frame.

## Lens Flare
Made the locking of the render targets (only used when not using Direct3D 9) read only.

## Load Manager Thread Coordination
Added this new advanced hack.

## Modern Resolution Support

* Added the `-noenumresolutions` command line argument. This stops the Mod Launcher and the hack from getting resolutions from your graphics card.
* Fixed an issue when your graphics card reports 5 resolutions or less where the ingame resolution picker would have invalid resolutions and there would be asserts when the game loaded a frontend file containing one when using the `-testing` command line argument.

## No Renderer
Added this awesome new setting hack. It's hidden by default.