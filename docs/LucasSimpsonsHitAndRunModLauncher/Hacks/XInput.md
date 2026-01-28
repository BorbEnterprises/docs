---
title: "XInput"
description: "This hack makes the game use XInput instead of DirectInput for controllers/gamepads."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 393 # 1.23
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack makes the game use XInput instead of DirectInput for controllers/gamepads.

This has various advantages over DirectInput:

* Makes controller rumble work.
    * This can be disabled in the hack's settings.
* Makes the game compatible with Steam's controller support when launching the Mod Launcher through Steam as a non-Steam game.
* Makes it so you can plug in new controllers while the game is running.
   
Currently, DirectInput only controllers will not work with this hack enabled and only one trigger can be used at a time. You can bind actions to both but they cannot be pressed at the same time.

# Settings
## Button Names
This setting affects what names are used in the game's menus.

* [DirectInput button names](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/XInput/DirectInputButtonNames.png): These are what the original game uses and how the buttons were shown in Version 1.23 (except for the guide button which now shows as "J Button 10" instead of "J Guide").
* [Xbox 360 button names](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/XInput/Xbox360ButtonNames.png): These are like that of an Xbox 360 controller. This is now enabled by default.
* [Xbox One button names](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/XInput/XboxOneButtonNames.png): These are the same as Xbox 360 with "Back" and "Start" instead named "View" and "Menu" respectively.

**Defaults to Xbox 360.**

## Default Controls
This setting affects what the gamepad controls are set to when resetting the controls to their defaults via the ingame menu.

* PC controls: The PC version's original default controller mapping.
* Xbox controls: The Xbox version's controller mapping.

**Defaults to Xbox.**

## Rumble
Set whether or not controller rumble is enabled.

**Defaults to Enabled.**

## Independent Inputs
### Triggers
Set whether or not the triggers can be used simultaneously.

**Defaults to Enabled.**

### D-Pad Buttons
Set whether or not the D-Pad buttons can be used simultaneously.

**Defaults to Enabled.**

# Command Line Arguments
This hack is affected by certain [[../CommandLineArguments.md]] for the Mod Launcher.

# Version History
## Version 1.23.9
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.9/Hacks/XInput.md }}

## Version 1.23.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.1/Hacks/XInput.md }}