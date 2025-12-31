---
title: Hack Support
description: "This hack manages and co-ordinates all other hacks, provides shared patches/functionality to hacks, loads mods and provides the underlying virtual file system used by Mods and Hacks."
---

**This hack is [always enabled](all-hacks.md#always-enabled-hacks) when using the Mod Launcher.**

**This hack can be [required by a mod](all-hacks.md#mod-requirable-hacks) to be configured.**

This hack manages and co-ordinates all other hacks, provides shared patches/functionality to hacks, loads mods and provides the underlying virtual file system used by Mods and Hacks.

While Hack Support provides shared patches to other hacks, it only patches the game with the ones that are necessary for the loaded hacks as of Version 1.22.

# Features
These are features and changes provided by this hack.

<!-- TODO: Look into if this features list should be updated since 1.23 -->

* Adds various debug pages to [Debug Text](debug-text.md#registered-by-hack-support) if it's enabled.
* Changes the game's file not found message to [show a path and a retry button](/img/lucasmodlauncher/hacks/hack-support/fnf_message.png) instead of just a [file name](/img/lucasmodlauncher/hacks/hack-support/fnf_message_original.png).
    * This can be opted out of through a couple different means:
        * As of version 1.23, you can use the `-nohandlefilenotfound` [command line argument](../command-line-arguments.md#nohandlefilenotfound).
        * Enabling Debug Test and then enabling its "No Handle File Not Found" setting on the "Miscellaneous" page of its Mod Settings.
* Changes the title of the games window and the icon based on enabled mods.
    * The icon is changed to that of the current Main mod (if it has an icon) or if to the icon of a mod with an Edition specified (if there's no Main mod with an icon).
    * The title is prefixed with the title of the current Main mod (unless it also specifies an Edition).
    * The title is suffixed with an Edition in brackets if there's a mod enabled with one specified.
* Makes messages shown by the game and hacks support visual styles (if enabled on the game tab of [Launcher Settings](../settings.md)).
* Makes the game DPI Aware (if enabled on the game tab of [Launcher Settings](../settings.md)).
* Makes the game [show a message on startup](/img/lucasmodlauncher/hacks/hack-support/no-audio-device-message.png) if there are no audio devices or the Windows Audio service is not running instead of [crashing](/img/lucasmodlauncher/misc/no-audio-device-crash.png).
    * This can be opted out of with the `-noaudiodevicecheck` [command line argument](../command-line-arguments.md#noaudiodevicecheck).
* Makes the game show an [assertion failed dialog](/img/lucasmodlauncher/hacks/hack-support/merch_null.png) if the loaded save file has more rewards unlocked than are defined in the rewards file instead of the game crashing.
    * You can use the "Ignore" button to continue the game. Saving the game after doing so will cause the fact that the reward was unlocked to disappear from your save data.
* Makes the game get terminated if it takes more than 1 second to exit.
    * This is to stop the game from hanging in the background indefinitely hogging CPU which sometimes happens in this game. 
    * This will show an assertion failed message if you're using the `-testing` [command line argument](../command-line-arguments.md#testing).
* Makes the game reload car camera data when a car gets loaded (such as when calling it from the phone booth).
    * The game normally loads this data again but throws it away instead of keeping the new data.
    * This can be opted out of through a couple different means:
        * As of version 1.23, you can use the `-noreloadcarcameradata` [command line argument](../command-line-arguments.md#noreloadcarcameradata).
        * Enabling Debug Test and then enabling its "No Reload Car Camera Data" setting on the "Vehicles" page of its Mod Settings.
* Saves crash dumps when the game crashes (if enabled on the game tab of [Launcher Settings](../settings.md)).
* Terminates the game when it crashes (if enabled on the game tab of [Launcher Settings](../settings.md)).
* Shows a message when the game crashes (if enabled on the game tab of [Launcher Settings](../settings.md)).

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=HackSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `HackSupport.ini` and add the parameters necessary for your mod inside it.

**NOTE:** Despite this hack always being enabled, a mod must explicitly require it to configure it.

```ini
; [Miscellaneous] Section
	; OverrideTexture: Specify a texture name that will be forced for every non-animated shader.
	
[Miscellaneous]
OverrideTexture=Texture.png
```

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-hack-support) for the Mod Launcher.

# Debug Text Mode
This hack registers several [debug modes](debug-text.md#registered-by-hack-support) when used alongside [Debug Text](debug-text.md).

# Version History
This hack changes in practically every version of the Mod Launcher to accommodate other hacks so only some specific changes are listed here.

<!-- TODO: Look into this changelog at some point -->

## 1.25.1
{{ snippet lucasmodlauncher/versions/1.25.1/hack_hack-support }}

## 1.23.10
{{ snippet lucasmodlauncher/versions/1.23.10/hack_hack-support }}

## 1.23.9
{{ snippet lucasmodlauncher/versions/1.23.9/hack_hack-support }}

## 1.23.8

* Added `-debugstagechange`. This outputs information to the console when you change stages in a mission.
* Made asserts (when not using `-msvcasserts`) log to the log file (when "Logging" is enabled in the "Console and Logging" hack).
* Made crash/exception messages log to the log file (when "Logging" is enabled in the "Console and Logging" hack).

## 1.23.6

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

## 1.23.5
Made crashes in the hack window procedure event save a crash dump before terminating the game.

## 1.23.2

* Fixed a bug introduced in Version 1.23 where hacks were not notified when the Direct3D device was lost. 
    * This caused a crash when resetting the device (such as when changing the game's resolution) while saving screenshots or after the Lens Flare had been on screen.
        * There may have also been other crashes as a result of this issue.
* Made the crash message include " (C++ exception)" or " (integer division by zero)" after the code if it's one of those types of exceptions.
    * If it's a C++ exception, it also shows the [type name](https://docs.microsoft.com/en-us/cpp/cpp/type-info-class?view=vs-2017), value (if it's a long integer) and the result of [what](https://en.cppreference.com/w/cpp/error/exception/what) (if it's an `std::exception`).
* Made using the `-breakgame` and `-suspend` command line arguments together cause the message from `-suspend` to get shown by the Mod Launcher before resuming the injection thread (instead of being shown from inside the game process).
    * This also prevents the breakpoint from `-breakgame` from happening if there's a debugger attached to the game.

## 1.23

* Added the `-hookd3d` command line argument.
* Added the `-nohandlefilenotfound` command line argument.
* Added the `-nohardwareskinning` and `-hardwareskinning` command line arguments.
* Added the `-noreloadcarcameradata` command line argument.
* Fixed an issue where the Direct3D hook in this hack caused the game to reset the Direct3D device redundantly once at startup.
* Made this hack block the game from resetting the Direct3D device when it's not necessary.
    * Also added the `-noblockredundantreset` command line argument to opt out of this.
* Made the game terminate abruptly with no message or crash dump in the case that an exception occurs in the hack window procedure event (instead of letting Windows swallow the exception and likely cause corruption).

## 1.22.4
Added the `-breakgame`command line argument. This break points the game as soon as possible after Hack Support is loaded.

## 1.22.3

* Made it so certain types of crash (access violation, breakpoint and invalid instruction) show the type in the crash message.
    * Access violations also show if it was attempting to read or write as well as the address attempting to be read or written to.

## 1.22.1

* Added a `-noresourcemeta` command line argument. This disables this hack reading information out of the Meta files for Mods and Hacks.
* Increased the maximum length of property values in INI files from 511 characters to 32767 characters.

## 1.22

* Added a new "mods" page when Debug Text is enabled. This page lists all mods and mod hacks that are enabled.
* Added a `-nounrequesthackevents` command line argument. This makes it so hacks do not unrequest hack events they're not using after the first time they're told about them resulting in reduced efficency.
* Added a `-nohookd3d` command line argument. This disables the Mod Launcher hooking D3D and breaks functionality of numerous hacks. Fun!
* Added new "hacks", "shared hacks" and "hack events" pages that show up in Debug Text when using the `-testing` command line argument.
* Made the `-suspend` command line argument show its message earlier.
* Made the `-testing` command line argument show an assert if the game gets terminated because it took more than 1 second to exit.
* Made it so this hack only installs shared patches when they are necessary.
    * Also added "-installallsharedhacks". This makes all shared patches get installed regardless of whether or not they're actually in use.
* Made this hack show an assert if it tries to patch the game, call game code or read/write variables if there is no address for the current game version.
    * In the case of patches, the patch is also not applied. Otherwise, the game will probably crash after the assert.
    * This should never happen, probably.
    * Anyways, you can use `-ignoremissingaddresses` to disable this assert.

## 1.17
Made some debug asserts display more helpful error messages.

## 1.16
Made it take the game out of fullscreen when showing message windows.

## 1.15

* Fixed issues with making the game DPI aware.
* Now adds the title of the current main mod to the Game window title if one is enabled.

## 1.13
Made the game support DPIs other than 96.

## 1.12
Fixed a bug where a message saying "The game was terminated while Hack Support was initialising." would appear if the game's CD check failed.

## 1.2 or earlier
Added this hack.