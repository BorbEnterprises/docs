---
title: Events
description: "This page documents events in the game."
status:
    class: "wip"
---

This page documents events in the game.

These are used for various things such as [Type 0 Event Locators](/pure3d/chunk-types/chunk-3000005.md#type-0-event-locator).

# Event 2
Used in mission waypoints, this event doesn't seem to do anything when the locator is not being referenced by a stage.

# Event 4
Resets the player at the position of the locator itself and cars at the position of the locator's matrix when they enter its triggers.

# Event 5
Used on Interior Exit locators.

# Event 6
Plays an airvent sound and throws the player towards the towards the position of the locator itself when they enter any of its triggers.  

# Event 7
Triggers the event "L2_light_city_day" in "ambience.rms".

# Event 8
Triggers the event "L3_seaside_day" in "ambience.rms".

# Event 9
Triggers the event "L1_suburbs_day" in "ambience.rms".

# Event 23
Triggers the event "L2_railyard_day" in "ambience.rms".

# Event 46
Triggers the event "L1_Burns_Mansion_Interior" in "ambience.rms".  

# Event 48
Used for Jump Zone locators. <!-- TODO: Elaborate on the exact effects of this -->

# Event 61
Triggers the event "Social_Club" in the current music RMS.

Pushes "pause_region" to the top of the stack in "ambience.rms". It's unclear which music event is used to do this.

# Event 65
Modifies the lighting using the ARGB Integer color in the parameter field. 

# Event 79
Used to enter vehicles.

This type is dynamically created at runtime. The size of the Trigger Volume is based on a cube with Half Extents of X=1, Y=1, and Z=1. These are multiplied by the root Joint's (the Skeleton Joint with the same name as the car) rotation matrix. The Right X, Up Y, and Front Z components of the rotation matrix can be changed to scale the Trigger Volume.

# Event 170
Plays the sound associated with backing out of a menu.

Triggers on entry and exit of a Trigger.

# Event 171
Plays the sound associated with scrolling in a menu.

Triggers on entry and exit of a Trigger.

# Event 172
Plays the music cue associated with the newspaper spin. Switches to "FE_Trans02".

Triggers on entry and exit of a Trigger.

# Event 175
Plays the sound associated with selecting in a menu.

Triggers on entry and exit of a Trigger.

# Event 178
Plays the sound associated with pausing.

Triggers on entry and exit of a Trigger.

# Event 179
Plays the sound associated with unpausing.

Triggers on entry and exit of a Trigger.

# Event 180
Plays the sound associated with attempting to use a greyed-out menu item.

Triggers on entry and exit of a Trigger.

# Event 195
Plays an associated "dcar" line from the player character.

Triggers on entry and exit of a Trigger.

# Event 210
Activates various effects associated with obtaining Collector Cards. When applied to a Locator, it activates the text and image for a Card in the current Level,  and plays the character voice line and associated animation.

Triggers on entry and exit of a Trigger.

# Event 253
Plays the sound associated with being shocked by a wasp.

Triggers on entry and exit of a Trigger.

# Event 255
Plays the sound associated with picking up a mission collectible.

Triggers on entry and exit of a Trigger.

# Event 256
Starts a "Hit & Run!". When applied to a Locator, it only appears to activate the text and music cue.

Triggers on entry and exit of a Trigger.

# Event 257
Causes the player to be "BUSTED!". When applied to a Locator and not in a "Hit & Run!", it only appears to activate the text and music cue. While in a "Hit & Run!", entering a Trigger of this type will end the "Hit & Run!" and fine the player.

The Never Busted mod included with the Launcher makes use of [Custom Trigger Actions](../../lucasmodlauncher/hacks/custom-trigger-actions.md) to prevent this Event from activating.

Triggers on entry and exit of a Trigger.

# Event 258
Ends a "Hit & Run!". When applied to a Locator, it only appears to trigger a music transition.

Triggers on entry and exit of a Trigger.

# Event 259
Plays the warning noise used when the "Hit & Run!" meter is high. When applied to a Locator, it only triggers the sound.

Triggers on entry and exit of a Trigger.

# Event 266
Plays the music cue associated with winning a Bonus Game race. Switches to "Win_SS_Region".

Triggers on entry and exit of a Trigger.

# Event 267
Plays the music cue associated with losing a Bonus Game race. Switches to "Lose_SS_Region".

Triggers on entry and exit of a Trigger.

# Event 268
Plays the credits music. Switches to "Credits_region".

Triggers on entry and exit of a Trigger.

# Event 269
Plays the menu music music. Switches to "FE_region".

Triggers on entry and exit of a Trigger.

# Event 270
Plays the phone booth music. Switches to "Store_region".

Triggers on entry and exit of a Trigger.

# Event 272
Halts the current music track. Switches to "movie_region".

Triggers on entry and exit of a Trigger.

# Event 294
Causes the player character's mouth to move. This effect stacks, allowing repeated entry and exit to make the player character's mouth flap at absurd speeds.

Triggers on entry and exit of a Trigger.

# Event 295
Causes the player character's mouth to stop moving.

Triggers on entry and exit of a Trigger.

# Event 306
Plays the fanfare upon completing all Street Races. Switches to "Win_3Street_Races_region".

# Event 312
Repairs the player's vehicle.

# Event 313
Plays the sound associated with collecting a Wrench.

# Notes
This page is primarily based on in-game observations with additional details being obtained with [Debug Text](../../lucasmodlauncher/hacks/debug-text.md). 

As such, many of these events may have additional effects not listed here and this is also far from a complete list.
