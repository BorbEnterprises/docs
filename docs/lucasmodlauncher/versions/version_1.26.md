---
title: Version 1.26
description: "This update was released on February 27th, 2021."
authors: ["loren","lucasc190"]
---

**This update was released on February 27th, 2021.**

# Launcher
## General

* Fixed an issue where the Mod Launcher still [created a Direct3D 8 object](https://docs.microsoft.com/en-us/previous-versions/ms889029(v=msdn.10)), usually used for checking which MSAA levels are available, even when using the `-forcemsaa` command line argument.
* Fixed an issue where the Anti-aliasing hack would fail to load *and* [show a message](/img/lucasmodlauncher/misc/1.26_could_not_load_aa.png) if Direct3D 8 was unavailable when it should do so silently.
* Fixed possible memory corruption relating to [PROPVARIANT](https://docs.microsoft.com/en-us/windows/win32/api/propidlbase/ns-propidlbase-propvariant) when fixing pinned shortcuts and updating the Jump List.
* Updated the Mod Launcher's copyright year to 2021.
* Fixed possible memory corruption when getting the OS version for the user agent when not using the `-useragent` command line argument.
* Made the error message shown when failing to connect to Donut Team show the exception or HTTP status code.
* Made the Mod Launcher show [a warning](/img/lucasmodlauncher/misc/1.26_no_internal_name_warning.png) when attempting to compile a mod without an internal name.
	* Also added the `-nocompileinternalnamecheck` command line argument to opt out of this.
* Added the `-nomodenablewarnings` command line argument. This disables warnings shown when mods that specify one are ticked in the mods list.
* Updated cacert.pem.

## Main Window

* Fixed an issue where ampersands (&) in main mod titles were not escaped when showing the title of the main mod on the "Saved Games" and "Screenshots" items in the "Open..." menu.
	* This resulted in the ampersand not appearing and *sometimes* the next character being underlined.
		* This also meant the underlined character would act as a hotkey.

## Mods List
Added a "Show Saved Games" option when right clicking a selected mod in the Mods List with one or more main mods selected.

## Mod Settings
Made it so mod settings windows omit the label of settings that have a blank string as their `Title`.

## Launcher Settings
Made it so being requirable by hacks is no longer a reason for hacks to be listed on the Non-mod Hacks page.

## Localisation

* This version adds new language strings.
	* A new template language (Template_1.26.xml) was published on [this page](../localisation.md) including these new strings at the end of the file.
* Made it so you can seamlessly change the program's language without a restart.
* Made it so the current language file will get reloaded when the main window is focused if it changed.
* Made the error message shown when failing to load a language file have a Retry button.
* Fixed an issue where the error message shown when failing to load a language file on the Select Language window was not modal to the Select Language window.
	* This resulted in the Select Language window being focusable and interactive and possibly in an unstable state.
* Fixed an issue where failing to load a language file on the Select Language window didn't change the Language combo box back to the default English.

# Mod Features
{{ snippet lucasmodlauncher/versions/1.26/mod_features }}

# Hacks
## Additional Script Functionality
{{ snippet lucasmodlauncher/versions/1.26/hack_additional-script-functionality }}

## Analogue Mouse Input
Added this new advanced hack.

## Bug Fixes
{{ snippet lucasmodlauncher/versions/1.26/hack_bug-fixes }}

## Custom Car Support
{{ snippet lucasmodlauncher/versions/1.26/hack_custom-car-support }}

You can find out more about how to use the various new features of this hack on [its documentation page](/lucasmodlauncher/hacks/custom-car-support.md).

## Custom Files
{{ snippet lucasmodlauncher/versions/1.26/hack_custom-files }}

## Custom Limits
{{ snippet lucasmodlauncher/versions/1.26/hack_custom-limits }}

## Custom Text
{{ snippet lucasmodlauncher/versions/1.26/hack_custom-text }}

## Debug Checks
{{ snippet lucasmodlauncher/versions/1.26/hack_debug-checks }}

## Debug Text
{{ snippet lucasmodlauncher/versions/1.26/hack_debug-text }}

## Direct3D 9
{{ snippet lucasmodlauncher/versions/1.26/hack_direct3d-9 }}

## Discord Rich Presence
{{ snippet lucasmodlauncher/versions/1.26/hack_discord-rich-presence }}

## Hack Support
{{ snippet lucasmodlauncher/versions/1.26/hack_hack-support }}

## Hover Car Refraction
{{ snippet lucasmodlauncher/versions/1.26/hack_hover-car-refraction }}

## Modern Computer Support
{{ snippet lucasmodlauncher/versions/1.26/hack_modern-computer-support }}

## On Foot Orbit Camera
Added this hack.

This hack replaces the game's regular on foot camera with a more advanced, mouse-controllable, orbit camera.

You can find out more about this hack's various settings on [its documentation page](/lucasmodlauncher/hacks/orbit-camera.md).

## Refraction Shader Support
{{ snippet lucasmodlauncher/versions/1.26/hack_refraction-shader-support }}

## Skippable FMVs
Added this new hack.

This hack allows you to skip the game's opening FMV as well as FMVs in missions that you haven't seen before.

## Sphere Maps
{{ snippet lucasmodlauncher/versions/1.26/hack_sphere-maps }}

## Starting Coins
{{ snippet lucasmodlauncher/versions/1.26/hack_starting-coins }}

## Text Binary Search
Added this new hack.

This hack makes the game's text lookups use a more efficient binary search instead of looking through the entries in order until they find the one they're looking for.

This hack also sorts the text bible loaded out of `srr2.p3d` if it is not already sorted, like how Radical's is by default.