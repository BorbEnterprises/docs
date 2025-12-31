---
title: "#4: Adding Pedestrian Paths"
description: "This tutorial will guide you through adding pedestrian Paths to your map that allow pedestrians to spawn and walk around."
authors: ["loren"]
---

This tutorial will guide you through adding [pedestrian Paths](/pure3d/chunk-types/chunk-300000B.md) to your map.

These are pretty simple entities that allow pedestrians to spawn and walk around your map.

# Prerequisites

{{ snippet lucasmapbuilder/tutorial-prereqs }}
* Following the previous tutorials

# Step 1: Drawing paths {{ id step1 }}
Paths are represented in SketchUp as a series of **connected** lines in a group with a [Path group tag](/lucasmapbuilder/sketchup-models/group-tags/paths/path.md) applied to it.

It should be noted that pedestrians will only follow a path in one direction. Once they reach the end, they will start again from the beginning. For this reason, all paths should be **closed shapes** to assure they loop around it smoothly.

This also means there's two path tags to allow you to reverse the direction if nessecary:

* `Path`: The path will be followed in the direction you drew it.
* `PathReversed`: The path will be followed in the opposite direction.

Lastly, it should be noted that a path **cannot** have more than 32 points. The tool will ignore any that do as they would crash the game. <!-- TODO: Fact check if it actually ignores them -->

With all that in mind, go ahead and focus the `Terra` group and draw a couple closed shapes. Once you're done, delete the faces created inside them and group each shape separately.

![drawing paths gif](/img/lucasmapbuilder/tutorials/map-building/basics/adding-paths/s1_drawing.gif)

Then tag them with whatever [Path group tag](/lucasmapbuilder/sketchup-models/group-tags/paths/path.md) you'd like. This example uses both.

![path groups in outliner](/img/lucasmapbuilder/tutorials/map-building/basics/adding-paths/s1_outliner.png)

# Step 2: Build and check it out ingame {{ id step2 }}
There's no new rules to add for paths (they're handled by the `BaseZone` [ModelOutputInstructions](/lucasmapbuilder/xml-format/elements/outputs/modeloutputinstructions.md)) so you're actually already done!

Now it's time to run `Build.bat` to see if it works ingame.

If you've done everything right, the map should successfully build and your paths should work ingame:

![paths ingame](/img/lucasmapbuilder/tutorials/map-building/basics/adding-paths/s2_ingame.png)

**NOTE**: This demonstration uses the [Debug Text](/lucasmodlauncher/hacks/debug-text.md) hack included with the Mod Launcher to visualise the paths.

# You're done! {{ id end }}
That's it for this tutorial. You're now ready to move on to the next one.