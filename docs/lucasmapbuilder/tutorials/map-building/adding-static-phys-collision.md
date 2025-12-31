---
title: "#5: Adding Static Phys Collision"
description: "This tutorial will guide you through adding some Static Phys collision to your map. This type of collision is made up of boxes, cylinders and spheres."
authors: ["loren"]
---

This tutorial will guide you through adding some [Static Phys collision](/pure3d/chunk-types/chunk-3F00001.md) to your map.

This type of collision is made up of boxes, spheres and cylinders.

# Prerequisites

{{ snippet lucasmapbuilder/tutorial-prereqs }}
* Following the previous tutorials

# Step 1: Importing the collision components {{ id step1 }}
Much like Locators, collision objects have a few [Special Components](/lucasmapbuilder/sketchup-models/special-components.md):

* [CollisionBox](/lucasmapbuilder/sketchup-models/special-components.md#collisionbox): {{ snippet lucasmapbuilder/sketchup-models/special-components/collisionbox-desc}} 
* [CollisionCylinder](/lucasmapbuilder/sketchup-models/special-components.md#collisioncylinder): {{ snippet lucasmapbuilder/sketchup-models/special-components/collisioncylinder-desc}}
* [CollisionSphere](/lucasmapbuilder/sketchup-models/special-components.md#collisionsphere): {{ snippet lucasmapbuilder/sketchup-models/special-components/collisionsphere-desc}}

Go to **File > Import** and navigate to the **Components** folder next to the Map Builder's executable. From there, import "CollisionBox.skp" into your mod.

This will attach an instance of it on your cursor and you can go ahead and place it down anywhere on your terrain.

Repeat this for "CollisionCylinder.skp" and "CollisionSphere.skp".

Once you have all three components imported, go to the **Components** panel and click the little house icon to bring up the list of components in the current model. You should see all 3 of the components listed if you imported them correctly.

![components panel with collision components](/img/lucasmapbuilder/tutorials/map-building/adding-static-phys-collision/s1_components.png)

# Step 2: Adding some collision {{ id step2 }}
For this step, just go ahead and add a few of these collision components to your map.

![a few collision components](/img/lucasmapbuilder/tutorials/map-building/adding-static-phys-collision/s2_addingsome.png)

Once you add some, select all of them and right click to make them into a group.

In order to make this into [Static Phys collision](/pure3d/chunk-types/chunk-3F00001.md), you need to use the appropriately named [StaticPhys group tag](/lucasmapbuilder/sketchup-models/group-tags/collision/staticphys.md).

This tag has a few parameters that follow it:

{{ snippet lucasmapbuilder/sketchup-models/group-tags/staticphys-parameters }}

Radical typically uses `7`, `0` and `nosound` for these parameters. 

For the purposes of these tutorials, go ahead and use these values on your group. Once you're done that, your outliner should look something like this:

![static phys group in outliner](/img/lucasmapbuilder/tutorials/map-building/adding-static-phys-collision/s2_outliner.png)

If you created this group outside of your "Zone001" group, make sure to drag it inside it to make it apart of that zone.

# Step 3: Build and check it out ingame {{ id step3 }}
There's no new rules to add for static phys collision (they're handled by the `BaseZone` [ModelOutputInstructions](/lucasmapbuilder/xml-format/elements/outputs/modeloutputinstructions.md)) so you're actually already done!

Now it's time to run `Build.bat` to see if it works ingame.

If you've done everything right, the map should successfully build and your collision should work ingame:

![static phys ingame](/img/lucasmapbuilder/tutorials/map-building/adding-static-phys-collision/s3_ingame.png)

You should notice that your Static Phys collision is invisible ingame despite being visible in SketchUp. This is because the collision components use the [NonWorldMesh group tag](/lucasmapbuilder/sketchup-models/group-tags/entities/nonworldmesh.md) to tell the tool to not build their meshes as Static Entities.

# Extra: Flat End Cylinders {{ id extra }}
It should be noted that, by default, all [CollisionCylinder components]() build cylinders with rounded ends.

You can use the [FlatEnd group tag](/lucasmapbuilder/sketchup-models/group-tags/collision/components/flatend.md) on one of these components to make them have flat ends instead.

![flat end tag in outliner](/img/lucasmapbuilder/tutorials/map-building/adding-static-phys-collision/s4_flatend.png)

# You're done! {{ id end }}
That's it for this tutorial. You're ready to move on to the next one.