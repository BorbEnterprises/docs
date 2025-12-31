---
title: Version 1.22.4
description: "This update was released on April 25th, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on April 25th, 2019.**

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
* Made the Mod Launcher show a [message](/img/lucasmodlauncher/misc/hacksupport_not_loaded.png) after starting if Hack Support isn't loaded that tells you to make sure you extracted the ZIP file.
    * Also added the "-nohacksupportcheck" to disable this.
* Made the game show an [explanatory error message](/img/lucasmodlauncher/hacks/hack-support/no-audio-device-message.png) if there's no audio output device (or the Windows audio service isn't running) instead of crashing.
    * Also added the `-noaudiodevicecheck` command line argument to disable this.
* Made it so "-allowignoremodconflicts" allows you to skip the error message the Mod Launcher shows when you're using the minimum install of the game.

## Launcher Settings

* Made it so the file name of the game executable is selected by default on the Game tab.
* Made it so this window will get wider if needed to accomodate larger buttons/text from language localisation.

## Localisation

* Made it so the Mod Launcher will show a language selection dialogue on first launch if there's any additional languages or on subsequent launches if the languages have changed.
    * Also added the `-noselectlanguage` command line argument. This disables this dialogue.
    * Also added the `-selectlanguage` command line argument. This forces this dialogue to show up.
* Made localisation extend to various messages from Hack Support.
    * Also added the `-nohacklanguagelocalisation` command line argument to opt out of this.
* Made certain proper nouns like the title of the Mod Launcher or "Donut Team" get substituted in various strings.
    * There is full backwards compatibility with the old formats of these strings so old language packs still work.

A new template language (Template_1.22.4.xml) was published on [this page](../localisation.md) including these new string formats as well as the original strings. The template also now indicates when strings were removed if they were in this update or any previous ones.

# Hacks
## Hack Support
Added the `-breakgame`command line argument. This break points the game as soon as possible after Hack Support is loaded.

## Additional Script Functionality
Fixed an assert when starting a mission that has an "insidetrigger" or "outsidetrigger" objective or condition on its first stage.

## Debug Checks
Locator Missing Detection is no longer referred to as experimental.