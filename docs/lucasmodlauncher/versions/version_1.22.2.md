---
title: Version 1.22.2
description: "This update was released on March 31st, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on March 31st, 2019.**

# Launcher
## General

* Added a new web requests system that supports asynchronous requests and using the system proxy (when using libcurl).
    * Also updated user interfaces that use web requests to be asynchronous.
    * Also added a `-noproxy` command line argument to bypass the system proxy.
* Made the Mod Launcher show mod/hack load errors sooner in certain cases.
    * Before compiling mods when using the `-compile` command line argument.
        * This means the Mod Launcher will no longer crash before telling you the load error in the event a mod fails to load while using this command line argument.
    * Before showing the Launcher Settings window when using the `-launchersettings` command line argument.
* Made the Mod Launcher's unhandled exception message have an "OK" and a "Cancel" button instead of just an "OK" button and made it try to continue when clicking "OK" instead of just terminating the program.

## Mod Settings
Fixed an issue where Text mod settings with Options specified had a custom context menu.

# Mod Features

* Added support for encrypting mods when compiling them.
    * This is enabled by default for mods that require this version or newer but it can also be opted into manually (which will also implicity make the mod require this version or newer).
    * This only encrypts text based files (.ini, .xml, .lua, .con, .mfk, .cho, .spt) by default.
        * Various new properties were added to the `[Compile]` section of mods to configure what gets encrypted.
    * Also added a `-forceencryption` command line argument so the Mod Launcher will always encrypt mods regardless of their RequiredLauncher or other criteria.

# Hacks
## Custom Trigger Actions

* Added a `Not` property on conditions that makes them return true when they are not met.
* Made the `BonusMission` property on `Mission` type `[Condition]` sections work as originally documented.
    * This value was documented as being a number from 1 to 5.
    * All previous versions were checking for 21 to 25 instead of 1 to 5.
    * For backwards compatibility reasons, it now checks for either set of numbers.