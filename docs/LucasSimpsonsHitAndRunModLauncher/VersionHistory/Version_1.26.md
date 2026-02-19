---
title: "Version 1.26"
description: "Changelog for Version 1.26 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on February 27, 2021.**

# Launcher
## General
* Fixed an issue where the Mod Launcher still created a Direct3D 8 object, usually used for checking which MSAA levels are available, even when using the `-forcemsaa` command line argument.
* Fixed an issue where the Anti-aliasing hack would fail to load and show a message if Direct3D 8 was unavailable when it should do so silently.
* Fixed possible memory corruption relating to PROPVARIANT when fixing pinned shortcuts and updating the Jump List.
* Updated the Mod Launcher's copyright year to 2021.
* Fixed possible memory corruption when getting the OS version for the user agent when not using the `-useragent` command line argument.
* Made the error message shown when failing to connect to Donut Team show the exception or HTTP status code.
* Made the Mod Launcher show a warning when attempting to compile a mod without an internal name.
	* Also added the `-nocompileinternalnamecheck` command line argument to opt out of this.
* Added the `-nomodenablewarnings` command line argument. This disables warnings shown when mods that specify one are ticked in the mods list.
* Updated `cacert.pem`.

## Main Window
* Fixed an issue where ampersands (&) in main mod titles were not escaped when showing the title of the main mod on the **Saved Games** and **Screenshots** items in the **Open...** menu.
	* This resulted in the ampersand not appearing and *sometimes* the next character being underlined.
		* This also meant the underlined character would act as a hotkey.

## Mods List
Added a **Show Saved Games** option when right clicking a selected mod in the Mods List with one or more main mods selected.

## Mod Settings
Made it so mod settings windows omit the label of settings that have a blank string as their `Title`.

## Launcher Settings
Made it so being requirable by hacks is no longer a reason for hacks to be listed on the Non-mod Hacks page.

## Localisation
* This version adds new language strings.
	* A new template language (Template_1.26.xml) was published on [Project:181] including these new strings at the end of the file.
* Made it so you can seamlessly change the program's language without a restart.
* Made it so the current language file will get reloaded when the main window is focused if it changed.
* Made the error message shown when failing to load a language file have a Retry button.
* Fixed an issue where the error message shown when failing to load a language file on the Select Language window was not modal to the Select Language window.
	* This resulted in the Select Language window being focusable and interactive and possibly in an unstable state.
* Fixed an issue where failing to load a language file on the Select Language window didn't change the Language combo box back to the default English.

# Mod Features
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/ModFeatures.md }}

# New Hacks
## Analogue Mouse Input
Added this new advanced hack.

## On Foot Orbit Camera
Added this hack.

This hack replaces the game's regular on foot camera with a more advanced, mouse-controllable, orbit camera.

## Skippable FMVs
Added this new hack.

This hack allows you to skip the game's opening FMV as well as FMVs in missions that you haven't seen before.

## Text Binary Search
Added this new hack.

This hack makes the game's text lookups use a more efficient binary search instead of looking through the entries in order until they find the one they're looking for.

This hack also sorts the text bible loaded out of srr2.p3d if it is not already sorted, like how Radical's is by default.

# Updated Hacks
## Hack Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/HackSupport.md }}

## Additional Script Functionality
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/AdditionalScriptFunctionality.md }}

## Bug Fixes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/BugFixes.md }}

## Custom Car Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/CustomCarSupport.md }}

## Custom Files
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/CustomFiles.md }}

## Custom Limits
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/CustomLimits.md }}

## Custom Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/CustomText.md }}

## Debug Checks
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/DebugChecks.md }}

## Debug Test
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/DebugTest.md }}

## Debug Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/DebugText.md }}

## Direct3D 9
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/Direct3D9.md }}

## Discord Rich Presence
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/DiscordRichPresence.md }}

## Hover Car Refraction
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/HoverCarRefraction.md }}

## Modern Computer Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/ModernComputerSupport.md }}

## Refraction Shader Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/RefractionShaderSupport.md }}

## Sphere Maps
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/SphereMaps.md }}

## Starting Coins
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.26/Hacks/StartingCoins.md }}