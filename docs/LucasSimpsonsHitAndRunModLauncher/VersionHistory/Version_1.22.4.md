---
title: "Version 1.22.4"
description: "Changelog for Version 1.22.4 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on April 25, 2019.**

# Launcher
## General
* Added the `-nocheckforupdates` command line argument. This prevents the Mod Launcher from checking for updates regardless of your setting.
* Added the `-language` command line argument. This allows you to override the language of the game.
  * This doesn't work in the original English release of the game.
  * This still requires you to provide the dialog RCF file for the language you're overriding to.
* Added the `-proxy` command line argument.
* Added the `-updatecheckurl` command line argument.
* Fixed a bug introduced in 1.13 where the Mod Launcher required Service Pack 1 of .NET 3.5 due to using functionality added in it.
* Fixed a crash in the Mod Launcher that occured when launching the game when there's no resolutions listed in the resolutions combo box and the windowed check box is checked but disabled.
* Made it so `lucasstuff.com` is considered a Donut Team domain.
* Made the Mod Launcher show a [message](/img/LucasSimpsonsHitAndRunModLauncher/HackSupportNotLoaded.png) after starting if Hack Support isn't loaded that tells you to make sure you extracted the ZIP file.
    Also added the `-nohacksupportcheck` command line argument to disable this.
* Made the game show an [explanatory error message](/img/LucasSimpsonsHitAndRunModLauncher/NoAudioDevice.png) if there's no audio output device (or the Windows audio service isn't running) instead of crashing.
    Also added the `-noaudiodevicecheck` command line argument to disable this.
* Made it so the `-allowignoremodconflicts` command line argument allows you to skip the error message the Mod Launcher shows when you're using the minimum install of the game.

## Launcher Settings
* Made it so the file name of the game executable is selected by default on the Game tab.
* Made it so this window will get wider if needed to accomodate larger buttons/text from language localisation.

## Localisation
* Made it so the Mod Launcher will show a language selection dialogue on first launch if there's any additional languages or on subsequent launches if the languages have changed.
    Also added the `-noselectlanguage` command line argument. This disables this dialogue.
    Also added the `-selectlanguage` command line argument. This forces this dialogue to show up.
* Made localisation extend to various messages from Hack Support.
    Also added the `-nohacklanguagelocalisation` command line argument to opt out of this.
* Made certain proper nouns like the title of the Mod Launcher or **Donut Team** get substituted in various strings.
    There is full backwards compatibility with the old formats of these strings so old language packs still work.

A new template language (Template_1.22.4.xml) was published on [Project:181] including these new string formats as well as the original strings. The template also now indicates when strings were removed if they were in this update or any previous ones.

# Updated Hacks
## Hack Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.4/Hacks/HackSupport.md }}

## Additional Script Functionality
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.4/Hacks/AdditionalScriptFunctionality.md }}

## Debug Checks
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.4/Hacks/DebugChecks.md }}