---
title: Version 1.22.1
description: "This update was released on March 7th, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on March 7th, 2019.**

# Launcher
## General

* Fixed a crash when failing to read/write a pinned shortcut.
* Fixed a crash when failing to reload mods when doing a full reload as a result of one or more mods being unable to be individually reloaded when a Meta.ini changed before launching the game or compiling mods.
* Made it so loading a hack with "-hack" or "-hacks" will make the hack take precedence over the default hacks.

# Hacks
## Hack Support
* Added a `-noresourcemeta` command line argument. This disables this hack reading information out of the Meta files for Mods and Hacks.
* Increased the maximum length of property values in INI files from 511 characters to 32767 characters.

## Custom Text
Removed this hack's length limit on strings, instead using the general limit (now 32767).