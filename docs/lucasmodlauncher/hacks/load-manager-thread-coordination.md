---
title: Load Manager Thread Coordination
description: "This hack replaces the game's code for coordinating its main thread and load manager thread."
---

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List (hidden by default).**

**This is an [advanced hack](all-hacks.md#advanced-hacks) that can be required by other hacks.**

This hack replaces the game's code for coordinating its main thread and load manager thread.

# Usage
This hack is used when "Load Files While Waiting" is enabled in the [Frame Limiter](frame-limiter.md) hack.

# Technical Details
The game does not intend its main thread and its load manager thread to execute simultaneously, instead intending each to only run when yieled to by the other.

This yielding is done by unlocking a critical section, sleeping for 0 milliseconds and then locking the critical section again. Sleeping for 0 milliseconds no longer has any effect as of Windows Vista / Windows Server 2003 (at least, not when the threads have an affinity of multiple processor cores).

The custom coordination this hack provides instead facilitates the yielding by using Windows event objects instead of a critical section. This should be equivalent to how the game is intended to work and, at least, similar to how the game runs on a single processor core and on Windows XP.

When [Frame Limiter](frame-limiter.md) and its [Load Files While Waiting](frame-limiter.md#load-files-while-waiting) setting are enabled, the imposing of the frame limit is integrated into the custom yielding logic to ensure that it does not block the load manager thread when possible. This mitigates slower load times when frame limiting and may allow faster load times than otherwise possible, at any given limited frame rate, without the setting enabled.

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-load-manager-thread-coordination) for the Mod Launcher.

# Version History
## 1.23.9
{{ snippet lucasmodlauncher/versions/1.23.9/hack_load-manager-thread-coordination }}

## 1.23.2
Added this hack.