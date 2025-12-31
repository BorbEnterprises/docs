---
title: "#3: Adding Fence Collision"
description: "This tutorial will guide you through adding Fence collision to your map to keep the player in bounds."
authors: ["loren"]
---

This tutorial will guide you through adding [Fence collision](/pure3d/chunk-types/chunk-3F00007.md) to your map.

Fence collision is infinite vertical collision that is only collidable on one side. These are typically used as the "walls" of the map so the player can't escape its bounds.

# Prerequisites

{{ snippet lucasmapbuilder/tutorial-prereqs }}
* Following the previous tutorials

# Step 1: Drawing fences {{ id step1 }}
Fence Collision is represented in SketchUp as a series of lines in a group with a [Fence group tag](/lucasmapbuilder/sketchup-models/group-tags/collision/fence.md) applied to it.

Since fences are one-way collision, which side is solid is determined by how you draw the lines and which tag you use on the group:

* `FenceCW`: The fences will face outwards when drawn in a clockwise motion.
* `FenceCCW`: The fences will face inwards when drawn in a clockwise motion.

For this map, you can simply draw a square around the edges. If you draw the lines in such a way that they create a face, be sure to delete that face. Once you're done, group the lines together. **Make sure to go in the same direction with all of the lines!**

To start, you'll want to focus the `Terra` group that your roads are in and draw 4 lines going around the bounds of the map. 

![drawing fence lines gif](/img/lucasmapbuilder/tutorials/map-building/basics/adding-fences/s1_drawing.gif)

Assuming you drew the lines in the same direction as the demonstration above (clockwise), you will want to tag use the `FenceCCW` group tag to make them face inwards towards the playable area.

![fence group in outliner](/img/lucasmapbuilder/tutorials/map-building/basics/adding-fences/s1_outliner.png)

# Step 2: Build and check it out ingame {{ id step2 }}
There's no new rules to add for the fences (they're handled by the `BaseZone` [ModelOutputInstructions](/lucasmapbuilder/xml-format/elements/outputs/modeloutputinstructions.md)) so you're actually already done!

Now it's time to run `Build.bat` to see if it works ingame.

If you've done everything right, the map should successfully build and your fences should work ingame:

![gif of homer running into the fences](/img/lucasmapbuilder/tutorials/map-building/basics/adding-fences/s2_running.gif)

**NOTE**: This demonstration uses the [Debug Text](/lucasmodlauncher/hacks/debug-text.md) hack included with the Mod Launcher to visualise the fences.

If the collision is backwards from what you'd expect, try swapping out the `FenceCCW` tag for `FenceCW` to flip it around.

# You're done! {{ id end }}
That's it for this tutorial. You're now ready to move on to the next one.