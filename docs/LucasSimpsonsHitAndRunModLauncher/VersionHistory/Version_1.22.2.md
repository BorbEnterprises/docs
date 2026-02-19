---
title: "Version 1.22.2"
description: "Changelog for Version 1.22.2 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on March 31, 2019.**

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
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.2/ModFeatures.md }}

# Updated Hacks
## Custom Trigger Actions
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22.2/Hacks/CustomTriggerActions.md }}