---
title: "Version 1.25"
description: "Changelog for Version 1.25 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on July 21, 2020.**

# Launcher
## General
* Made the Mod Launcher support .NET 4.0 and use it if it's available.
	* .NET 4.0 is installed by default on Windows 8 and newer.
	* .NET 3.5 is installed by default on Windows 7.
	* This means the Mod Launcher should no longer require a version of .NET that isn't installed by default on Windows 7 or newer.
	* Windows XP and Windows Vista users can install .NET 3.5 or .NET 4.0 to run the Mod Launcher.
	* Windows 7 users can optionally install .NET 4.0.
	* You can delete "Lucas Simpsons Hit & Run Mod Launcher.exe.config" out of the folder to opt out of this change.
* Made the Mod Launcher support running in Mono within Wine on Linux.
	* You can start it in Mono on Windows as well but this doesn't work very well.
* Made the Mod Launcher show [a message](/img/LucasSimpsonsHitAndRunModLauncher/WindowsEnvironmentMessage.png) and refuse to start if it's not running in a Windows environment (such as Mono on Linux but not within Wine).
	* Also added the `-nowindowscheck` command line argument to bypass this.
		* Bypassing this won't work particularly well.
	* Also added the `-spoofwindowscheck` command line argument to force the non-Windows environment behaviour.
		* This is useful to test the message when localising the program.
* Made it so the Mod Launcher no longer creates `%localappdata%\Lucas Stuff\Lucas' Simpsons Hit & Run Mod Launcher` on startup.
	* Now it will only get created when it's actually needed (when generating mod icons for the Jump List or the game window (when a Main mod or Edition mod with an icon is enabled and when not using `-nogamemodicon`)).
* Fixed an issue where the Mod Launcher could not load its hacks when running from a path containing characters not supported by the user's non-Unicode system locale.
	* For example: A path containing Chinese or Russian characters when using an English locale.
* Made the `-language` command line argument support `E`, `F`, `G` and `S` in addition to `0`, `1`, `2` and `4` respectively.

## Mods List
* Made it so the mods list no longer gets repopulated in various cases.
	* When disabling mods when on the Enabled category.
	* When removing mods from your Favourites when on the Favourites category.
	* When hiding mods when on categories other than Enabled.
	* When unhiding mods when on the Hidden category.
	* Instead, it just removes the mods that should no longer be listed.
	* This makes these actions faster and also makes it so they don't scroll the mods list to the top anymore.
* Made it so reloading individual mods no longer redundantly updates the mods list a second time.
	* This causes it to be slightly faster.

## Localisation
This version adds new language strings.

A new template language (Template_1.25.xml) was published on [Project:181] including these new strings at the end of the file.

# New Hacks
### No Bonus Game
Added this hack. This can be required by a mod to disable the bonus game.

# Updated Hacks
## Additional Script Functionality
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/AdditionalScriptFunctionality.md }}

## Custom Character Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/CustomCharacterSupport.md }}

## Custom Files
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/CustomFiles.md }}

### Custom Limits
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/CustomLimits.md }}

### Custom Shop Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/CustomShopSupport.md }}

### Debug Checks
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/DebugChecks.md }}

### Debug Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/DebugText.md }}

### File System RCFs
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/FileSystemRCFs.md }}

### Modern Computer Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/ModernComputerSupport.md }}

### No Introduction Movies
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/NoIntroductionMovies.md }}

### Skip Main Menu
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.25/Hacks/SkipMainMenu.md }}