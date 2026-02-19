---
title: "Version 1.20.1"
description: "Changelog for Version 1.20.1 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on December 31, 2018.**

# Launcher
## General
Made the Mod Launcher check if your mod's Meta.ini was updated since it was loaded when compiling.

## Localisation
This version adds 4 new language strings related to a compiling mod whose Meta.ini was modified since it was loaded.

A new template language (Template_1.20.1.xml) was published on [Project:181] including these new string formats as well as the original strings. The template also now indicates when strings were removed if they were in this update or any previous ones.

# Mod Features
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.20.1/ModFeatures.md }}

# New Hacks
## Override Shader Parameters
Added this new hack. This allows you to override any parameter in a shader from an XML file including ones that are normally forced on such as `2SID` (2-sided).

# Updated Hacks
## Aspect Ratio Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.20.1/Hacks/AspectRatioSupport.md }}

## Letterbox
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.20.1/Hacks/Letterbox.md }}