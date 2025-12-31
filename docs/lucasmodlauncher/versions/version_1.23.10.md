---
title: Version 1.23.10
description: "This update was released on March 10th, 2020."
authors: ["loren","lucasc190"]
---

**This update was released on March 10th, 2020.**

# Highlights
This update includes multiple security improvements that affect the Custom Files hack, we recommend you avoid using mods from untrusted sources in older versions.

# Launcher
## General

* Added the `-currentdirectory` command line argument. This allows you to specify a working directory for the Mod Launcher.
	* This was required for changes to the Discord Rich Presence hack listed below.
* Fixed an issue where screen readers (such as Windows Narrator) would refer to the Resolution combo box as the text of the update hyperlink instead of "Resolution".
	* The text of the update hyperlink would be "Placeholder" if it hadn't been shown yet.
* Updated the Mod Launcher's copyright year to 2020.
* Fixed a bug introduced in 1.23.2 where using 150% text size in Windows caused button and label text to be too big.

## Main Window

* Fixed an issue where the resolution list was being updated when enabling/disabling mods and after changing mod settings.
* Added a "Custom..." option to the resolution dropdown.

## Mod Settings

* Made it so these windows do not show a Reset button if none of the settings can be reset.
	* Such as when they all have `NoReset=1` or they're all `Label` type settings.
* Added various command line arguments that affect the appearance of these windows.
	* `-vistastylemodsettings`: This makes the area above the buttons have a different coloured background with a separator edge in between the two sections.
		* Also added `-vistastyleedge` to customise the size of the separator edge when this is enabled.
	* `-modsettingsicon`: Shows the mod's icon to the left of the settings.
		* Also added `-modsettingsiconsize` to customise the size of the icon when this is enabled.
	* `-nomodsettingsresetbutton`: Removes the reset button.
	* These can all be used together along with the existing `-noboldsettings` command line argument to make these windows [look how they did in Versions 1.5 through 1.9](/img/lucasmodlauncher/misc/old_modsettings_in_1.23.10.png).
* Made it so these windows are centred to the main window of the Mod Launcher instead of the screen.
* Made it so `Label` "settings" with a `URL` now show their `URL` in the tooltip.
	* If a `Tooltip` is also specified, it will be shown after this.

## Localisation
This version adds a couple new language strings related to new mod features.

A new template language (Template_1.23.10.xml) was published on [this page](../localisation.md) including these new strings at the end of the file.

## Configurations

* Fixed an issue where a configuration (and by extension the Mod Launcher window) could have the icon of the wrong edition mod when multiple edition mods are enabled and no main mods are enabled.
* Fixed an issue where mod icons were 16x16 on the Manage Configurations window regardless of your DPI.

# Mod Features
{{ snippet lucasmodlauncher/versions/1.23.10/mod_features }}

# Hacks
## General

* Blocked access to `Settings.ini` within the Virtual File System.
* Made Discord Rich Presence and NVIDIA Highlights support non-ASCII characters in the window title.
	* The game window itself still does not support non-Windows-1252 characters and will show them as question marks.
* Added a "Disable Anti-aliasing While Resizing" setting to the Resizable Window hack that disables the Anti-aliasing hack while resizing.
	* This does not apply to anti-aliasing enabled by the graphics driver or other third party programs.
	* This defaults to being enabled.

## Hack Support
{{ snippet lucasmodlauncher/versions/1.23.10/hack_hack-support }}

## Custom Files
{{ snippet lucasmodlauncher/versions/1.23.10/hack_custom-files }}

## Custom Limits
{{ snippet lucasmodlauncher/versions/1.23.10/hack_custom-limits }}

## Debug Checks
{{ snippet lucasmodlauncher/versions/1.23.10/hack_debug-checks }}

## Debug Test
{{ snippet lucasmodlauncher/versions/1.23.10/hack_debug-test }}

## Debug Text
{{ snippet lucasmodlauncher/versions/1.23.10/hack_debug-text }}

## Discord Rich Presence
{{ snippet lucasmodlauncher/versions/1.23.10/hack_discord-rich-presence }}

## NVIDIA Highlights
{{ snippet lucasmodlauncher/versions/1.23.10/hack_nvidia-highlights }}