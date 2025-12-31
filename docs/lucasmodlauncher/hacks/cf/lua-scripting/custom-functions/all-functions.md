---
title: All Custom Lua Functions
sidebar_label: All Functions
description: "This page documents all the custom Lua functions provided by custom files."
---

This page documents all the custom Lua functions provided by custom files.

# General Functions
## Alert

**Added in an unknown version.**

Shows a Windows message box for debugging purposes with an "OK" button.

[Learn more...](alert.md)

## ComparePaths

**Added in an unknown version.**

Compares two paths.

[Learn more...](comparepaths.md)

## Confirm

**Added in an unknown version.**

Shows a Windows message for debugging purposes with an "OK" button and a "Cancel" button.

[Learn more...](confirm.md)

## DirectoryGetEntries

**Added in an unknown version.**

Iterates a directory using the specified callback until that callback no longer returns true.

[Learn more...](directorygetentries.md)

## DirectoryRecursiveCreate

**Added in an unknown version.**

Recursively creates directories with the given path.

[Learn more...](directoryrecursivecreate.md)

## Exists

**Added in an unknown version.**

Returns whether or not the specified path exists.

[Learn more...](exists.md)

## FixSlashes

**Added in an unknown version.**

Returns a version of the given path with modified slashes.

[Learn more...](fixslashes.md)

## GetEnabledMods

**Added in an unknown version.**

Calls the given callback function for each mod that is enabled.

[Learn more...](getenabledmods.md)

## GetFileExtension

**Added in an unknown version.**

Returns the file extension of the specified path.

[Learn more...](getfileextension.md)

## GetFileName

**Added in an unknown version.**

Returns the file name of the specified path including the extension.

[Learn more...](getfilename.md)

## GetLauncherVersion

**Added in Version 1.19.**

Returns the current version of the Mod Launcher.

[Learn more...](getlauncherversion.md)

## GetMainMod

**Added in Version 1.19.**

Returns the name of the current main mod.

[Learn more...](getmainmod.md)

## GetModName

**Added in an unknown version.**

Returns the InternalName of the current mod.

[Learn more...](getmodname.md)

## GetModPath

**Added in an unknown version.**

Returns the path to a mod within the [Virtual File System](../../virtual-file-system.md).

[Learn more...](getmodpath.md)

## GetModTitle

**Added in an Version 1.22.**

Returns the title of a mod.

[Learn more...](getmodtitle.md)

## GetModVersion

**Added in an Version 1.22.**

Returns the version of a mod.

[Learn more...](getmodversion.md)

## GetPathParent

**Added in an unknown version.**

Returns the parent path of the specified file path.

[Learn more...](getpathparent.md)

## GetSetting

**Added in an unknown version.**

Returns the value of a setting in a mod.

[Learn more...](getsetting.md)

## GetSettings

**Added in Version 1.19.**

Returns the values of all of the settings of the a mod as a table.

[Learn more...](getsettings.md)

{{ summary lucasmodlauncher/hacks/cf/lua-scripting/custom-functions/getshared | 2 | Learn more... }}

## GetTime

**Added in an unknown version.**

Returns the amount of seconds the game has been running for.

[Learn more...](gettime.md)

{{ summary lucasmodlauncher/hacks/cf/lua-scripting/custom-functions/isdemo | 2 | Learn more... }}

## IsHackLoaded

**Added in Version 1.15.2.**

Returns whether or not a hack is loaded.

[Learn more...](ishackloaded.md)

## IsLegacyOutput

**Added in Version 1.23.9.**

Detects whether or not the `-legacyoutput` command line argument is in use.

[Learn more...](islegacyoutput.md)

## IsModEnabled

**Added in an unknown version.**

Returns whether or not a mod, mod hack or framework is enabled.

[Learn more...](ismodenabled.md)

## IsTesting

**Added in Version 1.19.**

Returns whether or not the user is currently using the [-testing](../../../../command-line-arguments.md#testing) command line argument on the Mod Launcher.

[Learn more...](istesting.md)

{{ summary lucasmodlauncher/hacks/cf/lua-scripting/custom-functions/pause | 2 | Learn more... }}

## ReadFile

**Added in an unknown version.**

Read a file at the given path.

[Learn more...](readfile.md)


{{ summary lucasmodlauncher/hacks/cf/lua-scripting/custom-functions/readfileoffset | 2 | Learn more... }}

## RemoveFileExtension

**Added in an unknown version.**

Returns the given file path or file name without the file extension.

[Learn more...](removefileextension.md)

## WildcardMatch

**Added in an unknown version.**

Compare text using a wildcard.

[Learn more...](wildcardmatch.md)

# Path Handler Functions
These functions can only be called with a [Path Handler](../path-handler-scripts.md) script.

## GetPath

**Added in an unknown version.**

Returns the path of the file being requested.

[Learn more...](getpath.md)

## IsWriting

**Added in an unknown version.**

Returns whether or not the game is requesting the file in order to write to it.

[Learn more...](iswriting.md)

## Output

**Added in an unknown version.**

Output data to a virtual file.

[Learn more...](output.md)

## Redirect

**Added in an unknown version.**

Redirect the file being requested to a different path.

[Learn more...](redirect.md)

## UseCallbacks

**Added in Version 1.19.**

Builds a file as the game requests it using callback functions.

[Learn more...](usecallbacks.md)