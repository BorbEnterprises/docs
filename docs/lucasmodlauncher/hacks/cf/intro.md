---
title: Custom Files
sidebar_label: Introduction
description: "This hack allows mods to provide custom files without modifying the game install."
---

**This is a [mod requirable hack](../all-hacks.md#mod-requirable-hacks) that must be required by a mod to be enabled.**

This hack allows mods to provide custom files without modifying the game install.

It also allows mods to handle the game requesting files with Lua scripts which allows for a number of powerful features.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomFiles
```

Your mod must provide one of the following things when requiring this hack:

* `CustomFiles.ini`
* `CustomFiles.lua`
* A `CustomFiles` folder.
* An `AdditionalFiles` folder.

# Configuring This Hack
To configure this hack, create a file named `CustomFiles.ini` and add the parameters necessary for your mod inside it.

```ini
[Miscellaneous]
; OccludedPath
; 	Occlude a file from the game's view, this will make the game think it doesn't exist. Be careful with this. 
; 	Repeatable to occlude multiple files.
OccludedPath=path\\to\\file.p3d

; ReadOnly
; 	Prevents the game from writing to a file, but it can still read it. 
; 	Repeatable to make multiple files read only.
ReadOnly=path\\to\\file.p3d

; SuppressedPath
; 	Tries to prevent the game from loading a file. 
; 	Repeatable to suppress multiple files.
SuppressedPath=path\\to\\file.p3d
	
[PathRedirections]

; PATH_TO_FILE
; 	Redirect the file on the left to the path on the right.
;	Repeatable to redirect multiple files.
art\\frontend\\dynaload\\images\\license\\*.p3d=art\\license\\license.p3d

[PathHandlers]
; PATH_TO_FILE
; 	Specify a file path that, when requested, will cause a Lua Path Handler script to be executed.
; 	Repeatable to handle multiple files.
art\\cars\\family_v.p3d=Resources/scripts/handlers/famil_v.lua

[AdditionalFiles]
; PATH_TO_FILE
; 	Specify a file on the right that will also be loaded when the left file is loaded.
;	Repeatable for the same base file or for any number of different files.
art\\cars\\famil_v.p3d=art\\cars\\famil_vH.p3d
```

\* Wildcard can be used in a path to indicate anything of any length.
? Wildcard can be used in a path to indicate anything of a set length.

# Folders
## CustomFiles
The main folder for this hack is one called "CustomFiles". This folder allows mods to override files in the base game. 

For example, a mod with a custom version of the Family Sedan at the path `CustomFiles\art\cars\famil_v.p3d` will override the game's original model for it.

## AdditionalFiles
Mods can also use a folder named "AdditionalFiles" is similar to "CustomFiles" but instead of overriding the files, it makes the game load the original file and the custom file. 

This functionality can break the game in a number of cases such as when it is used on a sound script (`.spt`).

## Resources
Lastly, mods that use this hack's [Lua Scripting](lua-scripting/intro.md) are expected to use a folder named "Resources" for any Lua scripts (besides `CustomFiles.lua`) and any other files that are exclusively redirected to or read by Lua scripts.

# Lua Scripting
For more detailed information, see [Lua Scripting](lua-scripting/intro.md).

# Version History
## 1.26
{{ snippet lucasmodlauncher/versions/1.26/hack_custom-files }}

## 1.25
{{ snippet lucasmodlauncher/versions/1.25/hack_custom-files }}

## 1.24
{{ snippet lucasmodlauncher/versions/1.24/hack_custom-files }}

## 1.23.12
{{ snippet lucasmodlauncher/versions/1.23.12/hack_custom-files }}

## 1.23.10
{{ snippet lucasmodlauncher/versions/1.23.10/hack_custom-files }}

## 1.23.9
{{ snippet lucasmodlauncher/versions/1.23.9/hack_custom-files }}

## 1.23.8

* Made it so the start of Lua file names are truncated instead of the end.
	* Also added `-notruncateluafilenamestart` to opt out of this change.
* Made various improvements to Lua execution errors.
	* They now include the title of the mod that executed the script.
	* They now include a stack trace.
		* Also added `-noluastacktrace` to opt out of this addition.
	* They now get logged to the log files (when "Logging" is enabled in the "Console and Logging" hack).
* Made various improvements to Lua load errors.
	* They now include the title of the mod that loaded the script.
	* They now get logged to the log files (when "Logging" is enabled in the "Console and Logging" hack).

## 1.19
### General

* Made CustomFiles.lua execute after all hacks that are supposed to be loaded are loaded.
* Made this hack only mount "CustomFiles" folders that exist.
    * This change can dramatically improve performance if you have lots of mods enabled but only a few have CustomFiles folders (like Mod Hacks for instance).

### Lua Scripting

* Added `GetLauncherVersion`. This returns the current version of the Mod Launcher.
* Added `GetMainMod`. This returns the InternalName of the current main mod (if there is one).
* Added `GetSettings`. This returns the settings of the current mod (or the specified mod) in a Lua table.
* Added `IsTesting`. This checks if the user is has the Mod Launcher's testing mode enabled.
* Added `UseCallbacks`. This is an advanced function for handling files with Lua that may or may not have a use case.
* Fixed an issue where "ComparePaths" was always case sensitive and always slash sensitive.

## 1.13.2
### General
Fixed a crash when redirecting files loaded by frontend pages.

## 1.13
{{ snippet lucasmodlauncher/versions/1.13/hack_custom-files }}

## 1.12.1
### Lua Scripting
Fixed a bug where using `GetSetting` on an `Integer` type `Number` setting would return a number.

## 1.12
{{ snippet lucasmodlauncher/versions/1.12/hack_custom-files }}

## 1.2 or earlier
Added this hack.