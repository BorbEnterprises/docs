---
title: "Known Issues"
description: "Known issues in Lucas' Simpsons Hit & Run Mod Launcher and their status."
authors: [ 2 ]
---

This page documents known issues in Lucas' Simpsons Hit & Run Mod Launcher.

The known issues here are reflective of the current version of the Mod Launcher.

# Launcher
## About Window
* The ampersand is missing from the title of the program on this window.
	* **Introduced**: Version 1.27
	* **Status**: Investigating

# Hacks
## Aspect Ratio Support
* The new Analogue Speedometer and Frame Rate Counter hacks are scaled incorrectly with certain aspect ratios.
	* **Introduced**: Version 1.27
	* **Status**: Investigating

## Cheat Keys
* The Toggle Vehicle Visibility key does not persist through changing the current camera.
	* **Introduced**: Version 1.27
	* **Status**: Investigating

## Dear Imgui
* Certain elements or text, such as the chat box in the Multiplayer hack, may overflow ImGui related containers slightly in Direct3D 8.
	* **Introduced**: Version 1.27
	* **Status**: Investigating

## Discord Rich Presence
* The game will crash on startup if you have a main mod enabled that does not have a `Title` set in its Meta.ini
	* **Introduced**: Version 1.27
	* **Status**: Fixed in Future Update

## Multiplayer
* The game may crash when certain HUD icons are updated at the server's request.
	* **Introduced**: Version 1.27
	* **Status**: Fixed in Future Update

## No Explosion Exit Delay
* Blowing up your car by entering the UFO’s tractor beam creates a vehicle you cannot enter.
	* **Introduced**: Version 1.27
	* **Status**: Investigating