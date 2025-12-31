---
title: XInput
description: "This hack makes the game use XInput instead of DirectInput for controllers/gamepads."
---

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List.**

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

* [DirectInput button names](/img/lucasmodlauncher/hacks/xinput/bnames_dinput.png): These are what the original game uses and how the buttons were shown in Version 1.23 (except for the guide button which now shows as "J Button 10" instead of "J Guide").
* [Xbox 360 button names](/img/lucasmodlauncher/hacks/xinput/bnames_x360.png): These are like that of an Xbox 360 controller. This is now enabled by default.
* [Xbox One button names](/img/lucasmodlauncher/hacks/xinput/bnames_xone.png): These are the same as Xbox 360 with "Back" and "Start" instead named "View" and "Menu" respectively.

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
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-xinput) for the Mod Launcher.

# Version History
## 1.23.9

{{ snippet lucasmodlauncher/versions/1.23.9/hack_xinput }}

## 1.23.1

* Added a "Button Names" setting.
* Added a "Default Controls" setting.
* Added two new settings to allow you to use both triggers simultaneously and multiple D-pad buttons simultaneously. These are both enabled by default.
* Added a `-noxinput` command line argument. This makes it so the hack does not make the game use XInput.
    * Despite this seeming counter-intuitive, it would still allow the other features of the hack to work while Windows' XInput-to-DirectInput backwards compatibility handles inputs.
* Added a `-noxinputdisable` command line argument. This makes it so XInput does not get disabled when the window is defocused.
* Fixed an inconsistency with the function used when [XInputEnable](https://docs.microsoft.com/en-au/windows/desktop/api/xinput/nf-xinput-xinputenable) is not available or when using the `-noxinputenable` command line argument.
* Fixed an issue where the Y (vertical) axis of the right stick was inverted.
    * This fix will require you to manually fix your control bindings.

## 1.23
Added this hack.