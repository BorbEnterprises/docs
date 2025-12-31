---
title: Version 4.0-L2PB2
description: "This update was released on September 8th, 2019."
---

**This update was released on September 8th, 2019.**

# General

* Now requires Version 1.23.5 of the Mod Launcher.
* Increased the physics prop limit further to potentially resolve a rare crash.
* Removed a comma from the global message used for out-of-vehicle conditions.

# Cars

* Ambulance
	* Extended the black void in the back to be visible when looking at the car from the sides.
* Dolph's Sedan
	* Fixed alpha issues with the roof.
	* Fixed a seam on the wheels.
	* Fixed an issue where the axles extended slightly out of the wheels.
	* Fixed the damaged hood texture being incorrect.
	* Made it so the driver side mirror is not damaged.
	* Made it so the rear passenger side window has glass instead of cardboard.
	* Removed the crate from the trunk.
	* Slightly increased the top speed.
* Li'l Lightnin'
	* Lowered the quality of some textures so they fit in better with the rest of the game world.
* Moe's Sedan
	* Fixed alpha issues with the roof.
	* Fixed a seam on the wheels.
	* Fixed an issue where the axles extended slightly out of the wheels.

# Characters

* Reduced the price of Homer's Gold costume from 1500 to 1000.
* Reduced the price of Bart's Silver costume from 2000 to 1500.

# Frontend
Fixed bleeding colors on the edges of the newspaper sprites.

# Taxi Missions

* Added an additional stage at the end that prompts you to restart the mission if you'd like to play again.
* Increased the base payout by 50%.

# Level 1
## Map
* Professor Frink's House
	* Added collision to the hedges and the top of the garage.
	* Changed the model of the door.
	* Reduced the size of the chip on the corner of the house.

# Level 2
## Collectibles
Added a new gag.

## Map

* DMV
	* Added an additional box near the DMV where you could walk through a wall.
	* Adjusted the position of the bus in the side of the DMV to make it easier to get on the roof.
* Downtown
	* Added a camera trigger on the rooftops near the Police Station to make it easier to see what you're doing.
	* Added better collision to the Krusty Burger and a cola crate on top.
* Stadium
	* Added US flags to the top.
	* Rotated the lights by 15 degrees.
* Town Hall
	* Added collision to the skin shop.
	* Fixed an issue where some collision on the cubicles did not work correctly by increasing a limit.
	* Improved the ground collision around the building to match the shape of the building and have the appropriate surface types inside.
* Other
	* Removed the guardrail near Moe's and the LBSC.

## Mission 2

* Changed various objective messages used during this mission.
* Changed where Kearney gets hidden so you can't run into a duplicate of him by driving to the police station on the first stage.
* Improved the camera angle when talking to Ralph.
* Made it so Bart will not say any mission victory dialogue at the end of this mission.
* Redesigned the mission to potentially fix a rare crash.
	* Made it so the forced car is not repositioned and you are not automatically placed into it after talking to Ralph.
		* This is to avoid using a script command that seems to crash the game on rare occasions in forced car missions.
	* Added a get-in stage to accomodate that change.
	* Changed it so the Hit & Run will start when getting back in the car (instead of when picking up the fireworks) to accomodate that change.

## Mission 4

* Added a condition to allow you to lose the race at the start.
* Swapped the order of the dialogue played when Snake hits Wiggum with his car.

## Mission 5

* Changed various objective messages used during this mission.
* Changed the HUD icon for the Drive to the Trainyard stage on Hellfish.
* Fixed a crash when starting this mission after having played the Taxi Mission.
* Redesigned the mission to potentially fix a rare crash.
	* Made it so the forced car is not repositioned and you are not automatically placed into it.
		* This is to avoid using a script command that seems to crash the game on rare occasions in forced car missions.
	* Added a couple additional pieces of flatmeat to the route used on Normal mode to accomodate that change.

## Mission 6
Added the Cement Mixer to block the dirt jump shortcut.

## Mission 7
Adjusted a couple of the routers so they're no longer floating in the air.

## Bonus Mission

* Changed most of the on foot objective types so the game doesn't take control of the camera during them.
* Made it so the inside trigger condition in the offices does not show a message.
* Made it so the mission will never select the same tile pattern twice in a row.
* Redesigned the mission to potentially fix a rare crash.
	* Made it so the forced car is not repositioned and you are not automatically placed into it after exiting the treasure room.
		* This is to avoid using a script command that seems to crash the game on rare occasions in forced car missions.
	* Added a get-in stage to accomodate that change.

## Taxi Mission

* Adjusted the time on Homer's Police Station to DMV route.
* Fixed a mistake where an alternate Homer costume did not use Homer's HUD icon.
* Fixed a mistake where one of Fat Tony's routes was marked as starting in the wrong zone.