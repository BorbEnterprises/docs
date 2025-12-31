---
title: Direct3D 9
description: "This hack makes the game use Direct3D 9 instead of Direct3D 8."
---

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List.**

This hack makes the game use Direct3D 9 instead of Direct3D 8.

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-direct3d-9) for the Mod Launcher.

# Version History
## 1.26.1
{{ snippet lucasmodlauncher/versions/1.26.1/hack_direct3d-9 }}

## 1.26
{{ snippet lucasmodlauncher/versions/1.26/hack_direct3d-9 }}

## 1.23.2

* Made this hack requirable by other hacks.
* Made unimplemented functions show a message saying they're not implemented with the the name (signature) of the function. These messages have an OK button to attempt to continue as well as a Close button to terminate the game.
    * This is instead of the generic assert they showed before.

## 1.23.1
Removed an [assert message](/img/lucasmodlauncher/misc/d3d9_assert.png) that would show up twice on exit when using ReShade and the `-testing` command line argument.

## 1.23
Added this hack.