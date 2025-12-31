---
title: Version 1.25.1
description: "This update was released on August 1st, 2020."
authors: ["loren","lucasc190"]
---

**This update was released on August 1st, 2020.**

# Launcher
## General

* Improved performance when working out what mod icon should be shown for configurations that don't have a main mod enabled on the main window, in the right click menu of the mods list, on the Manage Configurations window and when updating the Jump List.
* Made it so the configurations list in the right click menu of the mods list is only updated when opening the menu after one of the following circumstances has occurred since it was last opened:
	* Changing what main mods or edition mods are enabled for the current configuration.
	* Reloading mods.
	* Pressing "OK" on the "Manage Configurations" window.

## Mod Settings
Fixed an issue introduced in Version 1.24 where having a single mod setting with a wide label in a group or page by itself caused it to be smaller than it's supposed to be.

## Configurations
Fixed an issue where the Main mod or Edition mod's icon would not appear on the "Manage Configurations" window when importing a configuration that had a Main mod or an Edition mod enabled until the window was closed and re-opened.

# Mod Features
Fixed an issue introduced in Version 1.25 where compiling an encrypted mod resulted in a corrupt LMLM file.

See the `Encryption` property on [this page](/lucasmodlauncher/mods/configuring-mods.md#configuring-mods_compile-section) for details on when Mod Encryption is enabled.

# Hacks
## Hack Support
{{ snippet lucasmodlauncher/versions/1.25.1/hack_hack-support }}

## Additional Script Functionality
{{ snippet lucasmodlauncher/versions/1.25.1/hack_additional-script-functionality }}

## Debug Text
{{ snippet lucasmodlauncher/versions/1.25.1/hack_debug-text }}