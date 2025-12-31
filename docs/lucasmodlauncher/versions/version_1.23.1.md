---
title: Version 1.23.1
description: "This update was released on May 20th, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on May 20th, 2019.**

# Launcher
## Mod Settings
Fixed an issue where not enough space was allowed for bold tick box settings if they were not bold when you open a Mod Settings window.

# Hacks

## General
Fixed a [conflict](/img/lucasmodlauncher/misc/asf_debugtest_conflict.png) between Additional Script Functionality and Debug Test when the "Menus > Pause Menu > Pause Always Allowed" setting was enabled.

This message would show the conflict as being between Debug Test and Hack Support because it was caused by Additional Script Functionality being enabled and requesting functionality from the latter.

## Debug Text
Added a new "gamepads" debug mode.

## Direct3D 9
Removed an [assert message](/img/lucasmodlauncher/misc/d3d9_assert.png) that would show up twice on exit when using ReShade and the `-testing` command line argument.

## XInput

* Added a "Button Names" setting with 3 options: DirectInput, Xbox 360 and Xbox One. This affects what names are used in the game's menus.
    * [DirectInput button names](/img/lucasmodlauncher/hacks/xinput/bnames_dinput.png): These are what the original game uses and how it was in the previous version (except for the guide button which now shows as "J Button 10" instead of "J Guide").
    * [Xbox 360 button names](/img/lucasmodlauncher/hacks/xinput/bnames_x360.png): These are like that of an Xbox 360 controller. This is now enabled by default.
    * [Xbox One button names](/img/lucasmodlauncher/hacks/xinput/bnames_xone.png): These are the same as Xbox 360 with "Back" and "Start" instead named "View" and "Menu" respectively.
* Added a "Default Controls" setting with 2 options: PC and Xbox. This affects what your secondary controls are remapped to when using the game's "Restore All Defaults" option or when starting the game without any settings.
    * PC controls: The PC version's original default controller mapping.
    * Xbox controls: The Xbox version's controller mapping. This is now enabled by default.
* Added two new settings to allow you to use both triggers simultaneously and multiple D-pad buttons simultaneously. These are both enabled by default.
* Added a `-noxinput` command line argument. This makes it so the hack does not make the game use XInput.
    * Despite this seeming counter-intuitive, it would still allow the other features of the hack to work while Windows' XInput-to-DirectInput backwards compatibility handles inputs.
* Added a `-noxinputdisable` command line argument. This makes it so XInput does not get disabled when the window is defocused.
* Fixed an inconsistency with the function used when [XInputEnable](https://docs.microsoft.com/en-au/windows/desktop/api/xinput/nf-xinput-xinputenable) is not available or when using the `-noxinputenable` command line argument.
* Fixed an issue where the Y (vertical) axis of the right stick was inverted.
    * This fix will require you to manually fix your control bindings.