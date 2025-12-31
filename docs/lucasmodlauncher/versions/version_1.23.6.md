---
title: Version 1.23.6
description: "This update was released on September 24th, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on September 24th, 2019.**

# Hacks
## Hack Support

* Added [custom assert messages](/img/lucasmodlauncher/hacks/hack-support/assert_custom.png) that provide more information and save a crash dump.
    * Also added `-msvcasserts` to opt out of this entirely, instead using the [old MSVC style asserts](/img/lucasmodlauncher/hacks/hack-support/assert_msvc.png).
    * Also added `-noassertdump` to opt out of the crash dump specifically.
* Added a "keybinds" debug text mode.
    * This shows all keybinds registered by hacks and their bindings as well as whether or not they're currently pressed or being ignored.
* Added the `-debugkeybinds` command line argument. This makes it so this hack will print information about when keybinds are pressed, released and ignored to the console.
* Added the `-nolegacykeys` command line argument. This disables legacy keybinds.
    * All hacks except Debug Test use a new keybinds system added in Version 1.22 that is not affected by this argument.
        *  These are the ones shown on the new Debug Text page.
    * Debug Test still uses legacy keybinds for most of its functionality so it will get affected by this.
* Made it so the "hacks" debug text mode is available when not using the `-testing` command line argument.
    * By default, it only shows which hacks are loaded. The counts for how many times the various hacks have patched the game still require `-testing`.

## Bug Fixes
Added "Vehicles > Phone Booth Camera Pan Active Camera Change". 

This fixes a bug related to pressing the in-car change camera button during the phonebooth's camera pan. Without this bug fix, doing so will cancel the camera and switch your camera to the mouse controlled camera until the game changes your camera again (such as when getting in a car). If you use mission select to select a mission without getting in a car, you will be able to skip the next mission start camera.

We also added a `FixRelativeAnimatedCamCameraChange` property to the `[Camera]` section of `BugFixes.ini` to opt in to this.

This bug fix exists as a result of research done by [aldelaro5](https://twitter.com/aldelaro5).

## Console and Logging

* Made it so the hack will create multiple logs if its unable to write to the log file instead of showing an error message and not logging.
    * In these cases, the hack will just stick a number on the end of the file name like `Log (2).txt`.
* Fixed a crash when failing to open the log file with "Append" ticked.
* Fixed a crash when suppressing RCF files and asyncronous file load requests using Custom Files with this hack enabled and "Include > Hacks" ticked.

## Custom Trigger Actions

* Added a `CompletedMission` type for `[Condition]` sections.
    * This allows you to check whether or not a particular story mission, street race or bonus mission has been completed.
* Added a debug text mode that shows all registered conditions and whether or not they're currently met.

## Custom Vertex Shader Support
Fixed an issue where UVs were wrong on Old Primitive Groups that had a colour list when using the "spheremap" PDDI shader provided by the Sphere Maps hack and the "refract" PDDI shader provided by the Refraction Shader Support hack.

## Debug Checks

* Added a null-check of the car to the get position and get move speed functions of vehicle positional sound players with a new assert.
    * In other words, this assert can appear after the game tries and fails to play vehicle sounds.
    * Also added the `-novehiclepositionalsoundplayercarnullcheckasserts` command line argument to suppress the assert and allow the game to try to continue.

## No Busted Hit & Run Meter Reset
This makes it so the Hit & Run meter will not reset and the music will not end when you get busted by the police.

This hack expects the mod to actually set the decay to 0 alongside requiring it.

## No Hit & Run Music
Added this new setting and mod requirable hack. This disables the special music used during Hit & Runs.

## NVIDIA Highlights
Added a `-nocrashhighlight` command line argument that completely disables the type of highlight used when the game crashes.