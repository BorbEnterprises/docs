---
title: "Version 1.22.3"
description: "Changelog for Version 1.22.3 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on April 11, 2019.**

# Launcher
## General
* Added a `-noasyncwebrequests` command line argument to make it so all web requests are not asynchronous.
* Fixed a crash on startup when using Wine (and not using `-noappid`).
* Made it so the URL specified for the `-apiurl` command line argument gets changed from `https://` to `http://` when SSL isn't available from the usage of `-nossl` (or `-nocurl` on Windows XP) even if it's specified after it.
    * In previous versions, `-nossl` or `-nocurl` had to be specified first.

## Account Integration
* Added a `-account` command line argument to launch the Mod Launcher directly into the account window.
* Made it possible to close the account window while authenticating to cancel the authentication.
* Made it so your token gets reset after showing the **Your account's token has changed. You will need to re-enter the new one or login using your account details.** message.
* Removed the prompt before showing the account window on first launch and made the account window say **Skip** instead of **Close** when shown on first launch.

## Localization
This version introduces one new language string that language packs will need to be updated to include. This is the new **Skip** button that now appears on the Account Window on first launch.

A new template language (Template_1.22.3.xml) was published on [Project:181] including these new string formats as well as the original strings. The template also now indicates when strings were removed if they were in this update or any previous ones.

# Mod Features
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.3/ModFeatures.md }}

# Updated Hacks
## General
Fixed an issue with the new virtual filesystem where all files that were on a non-NTFS formatted drive (which is common with removable drives which often use FAT32 or exFAT) would fail to load causing a file not found error.

If you were using `-legacyfilesystem` to work around this issue, you should be able to safely remove it now for improved performance.

## Hack Support
* Made it so certain types of crash (access violation, breakpoint and invalid instruction) show the type in the crash message.
    * Access violations also show if it was attempting to read or write as well as the address attempting to be read or written to.

## Additional Script Functionality
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.3/Hacks/AdditionalScriptFunctionality.md }}

## Debug Checks
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.3/Hacks/DebugChecks.md }}