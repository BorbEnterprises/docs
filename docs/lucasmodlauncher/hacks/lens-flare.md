---
title: Lens Flare
description: "This hack enables the Lens Flare to work on PC just like the console releases of the game."
---

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List.**

This hack enables the Lens Flare to work on PC just like the console releases of the game.

# Showcase
## Base Game
![lens flare disabled](/img/lucasmodlauncher/hacks/lens-flare/disabled.png)

## Lens Flare Hack
![lens flare enabled](/img/lucasmodlauncher/hacks/lens-flare/enabled.png)

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-lens-flare) for the Mod Launcher.

# Version History
## 1.23.4
Removed an assert when failing to create the occlusion query when using `-testing`.

## 1.23.2
Made the locking of the render targets (only used when not using Direct3D 9) read only.

## 1.23

* Added a description to this hack.
* Made this hack work differently (using an [occlusion query](https://docs.microsoft.com/en-us/windows/win32/direct3d9/queries) instead of a lockable render target) when using [Direct3D 9](direct3d-9.md).
    * Also added a `-noocclusion` command line argument to opt out of this.
    * Also added a `-occlusionsleep` command line argument.

## 1.20

* Made Lens Flares not get enqueued if their World Sphere is deactivated.
    * Also added the `-deactivatedworldspherelensflares` command line argument to suppress this behaviour.
    * This fixes an issue where deactivating a world sphere would not deactivate its lens flare.

## 1.19
Added this hack.