---
title: Cheat Keys
description: "This hack adds a number of key binds that do various things that are effectively cheating."
---

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "General" page of the Mods List.**

This hack adds a number of key binds that do various things that are effectively cheating.

# Keybinds

| Key      | Function                                                                                     |
|----------|----------------------------------------------------------------------------------------------|
| 0        | Reset your Hit & Run meter.                                                                  |
| 2        | Double Speed.                                                                                |
| 3        | Stop your car.                                                                               |
| 5        | Invert your car's speed.                                                                     |
| 6        | Repair your car.                                                                             |
| 7        | Makes your car jump.                                                                         |
| F4       | Teleport your car to you.<br>Shows a phone booth interface if you do not already have a car. |
| F7       | Teleport your car or character forwards.                                                     |
| Shift+F4 | Shows a phone booth interface.                                                               |

# Settings
## Car Teleport Forward
### Distance
Configure the distance that the the F7 key teleports your car forward.

**Defaults to 8.**

### Reset Camera
Toggle whether or not the camera is reset when your car is teleported forwards with the F7 key.

**Defaults to Enabled.**

## On Foot Teleport Forward
### Distance
Configure the distance that the the F7 key teleports your character forward.

**Defaults to 2.**

### Reset Camera
Toggle whether or not the camera is reset when your character is teleported fowards with the F7 key.

**Defaults to Disabled.**

## Continuous
Makes cheat key actions happen continuously when their respective keys are pressed instead of just once.

**Defaults to Disabled.**

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-cheat-keys) for the Mod Launcher.

# Version History
## 1.23.5

* Made Shift+F4 to spawn a car not work when getting into a car.
* Made Shift+F4 to spawn a car not work during a forced car mission.
* Added `-forceallowcheatkeys` to opt out of the above two changes as well as a bunch of other safety checks including those added in Version 1.15.

## 1.22
Made F4 (or Shift+F4 if you already have a car like you're always supposed to unless you're playing SHAR MP) show the phone booth.

## 1.15

* Improved the handling of whether or not the player is in a vehicle.
* Improved the handling of the player's rotation when standing on movable objects such as platforms or cars.
* Made the various keys only work when Alt is not being pressed.
* Made the 0 key fully reset your Hit & Run instead of just depleting the meter.

## 1.13.1
Added a "Continuous" setting to make holding keys act as it did before Version 1.13.

## 1.13
Made keys only work once for each key press.

## 1.12

* Added the "Cheat Mods" category.
* Fixed a bug that prevented the 6 key from working in the Bonus Game.

## 1.2 or earlier
Added this hack.