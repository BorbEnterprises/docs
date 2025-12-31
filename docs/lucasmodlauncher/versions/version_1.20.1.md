---
title: Version 1.20.1
description: "This update was released on December 31st, 2018."
authors: ["loren","lucasc190"]
---

**This update was released on December 31st, 2018.**

# Launcher
## General
Made the Mod Launcher check if your mod's Meta.ini was updated since it was loaded when compiling.

## Localisation
This version adds 4 new language strings related to a compiling mod whose Meta.ini was modified since it was loaded.

A new template language (Template_1.20.1.xml) was published on [this page](../localisation.md) including these new strings at the end of the file.

# Mod Features
Added an `Alpha` property to `Colour` type settings.

# Hacks
## Aspect Ratio Support
Fixed an issue where the "Movie Letterbox Colour" setting let you pick an alpha.

## Letterbox
Fixed an issue where the "Colour" setting let you pick an alpha.

## Override Shader Parameters
Added this new hack. This allows you to override any parameter in a shader from an XML file including ones that are normally forced on such as "2SID" (2-sided).