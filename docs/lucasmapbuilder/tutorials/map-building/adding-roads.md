---
title: "#2: Adding Roads"
description: "This tutorial will guide you through expanding your map with new road meshes as well as a road network on top of them that allows for traffic to spawn and AI cars to navigate around."
authors: ["loren"]
---

This tutorial will guide you through expanding your map with new road meshes as well as a road network on top of them.

A road network is a series of interconnected [Roads](/pure3d/chunk-types/chunk-3000003.md) and [Intersections](/pure3d/chunk-types/chunk-3000004.md) that allows traffic to spawn and AI cars to navigate around. It's also used by the game's navigation system.

This tutorial will also cover making a custom HUD map [Mesh](/pure3d/chunk-types/chunk-10000.md) using your new road meshes.

# Prerequisites

{{ snippet lucasmapbuilder/tutorial-prereqs }}
* Following the previous tutorials

# Part 1: The SketchUp File {{ id part1 }}
## Step 1: Expanding the map {{ id step1 }}
In the previous tutorial, you created a map that was just a small square. This doesn't really have any space for a Road network so the first thing you'll want to do is expand the map a bit.

First focus the `Zone001` group. Then you should add some 12 meter wide rectangles to each side of the map and some 12x12 squares to each corner. It would also be good to make some [Materials](https://help.sketchup.com/en/sketchup/adding-colors-and-textures-materials) and color them differently so they can be told apart.

![new road meshes](/img/lucasmapbuilder/tutorials/map-building/basics/adding-roads/p1_s1_newroadmeshes.png)

After you make them, group the new shapes and name the group `Road [Intersect] [Road]`. The new [Road group tag](../../sketchup-models/group-tags/hudmaps/road.md) on the end is how you tell the tool to include this mesh on the HUD map in Radical's road color.
   
Once you've done that, your **Outliner** should look like this:

![new roads outliner](/img/lucasmapbuilder/tutorials/map-building/basics/adding-roads/p1_s1_outliner.png)

## Step 2: Making the roads {{ id step2 }}
Roads are very easy to create as they are just 1 or more connected lines with a special group name. Start by drawing 4 separate lines connecting the midpoints of each corner of the map. **Make sure not to do this inside the zone group.**

![road lines](/img/lucasmapbuilder/tutorials/map-building/basics/adding-roads/p1_s2_roadlines.png)

Then select each line individually and group it. Once you have 4 groups, name them with the following names:

* `Road001 [SimpleRoadPairRight] [3] [1] [12]`
* `Road002 [SimpleRoadPairRight] [3] [1] [12]`
* `Road003 [SimpleRoadPairRight] [3] [1] [12]`
* `Road004 [SimpleRoadPairRight] [3] [1] [12]`

In this case you use the [SimpleRoadPairRight group tag](../../sketchup-models/group-tags/roads/simpleroadpair.md) to tell the tool that you want this line to be made into 2 parallel roads going the opposite direction of one another. The `Right` part means cars will drive on the right side of the road though there is an equivalent [SimpleRoadPairLeft group tag](../../sketchup-models/group-tags/roads/simpleroadpair.md). 

The 3 parameters following that tag are as follows:

{{ snippet lucasmapbuilder/sketchup-models/group-tags/simpleroadpair-parameters }}

## Step 3: Making the intersections {{ id step3 }}
Intersections are also simple as they are just grouped circles. Draw 1 in each corner that fully covers the end of each road. 

**Make sure to delete the face in each one, leaving just the edges of the circles!**

![intersection circles](/img/lucasmapbuilder/tutorials/map-building/basics/adding-roads/p1_s3_intersections.png)

Now select each circle individually and group it. Name each one with some group tags as follows:
  
* `Intersection001 [Intersection]`
* `Intersection002 [Intersection] [Stop]`
* `Intersection003 [Intersection]`
* `Intersection004 [Intersection] [Stop]`

The [Intersection group tag](../../sketchup-models/group-tags/roads/intersection.md) tells the tool that these circles should become Intersections. 

This example also adds the [Stop group tag](../../sketchup-models/group-tags/roads/intersection.md#other-tags_stop) to the second and fourth intersections. This makes it so traffic will stop at these intersections instead of immediately continuing onto another road when they reach them.

## Step 4: Making the Terra group {{ id step4 }}
After you make the intersection groups, group all of them and the road groups from the previous step together and name the group `Terra`. 

This should leave your outliner looking like this:

![terra outliner](/img/lucasmapbuilder/tutorials/map-building/basics/adding-roads/p1_s4_outliner.png)

As you may recall, your [ModelOutputInstructions](/lucasmapbuilder/xml-format/elements/outputs/modeloutputinstructions.md) already selects a group by this name. This means these are already going to get built into your map's Terra file the next time you build it.

# Part 2: Configuring the Map Builder {{ id part2 }}
## Step 1: Including Base HUD Map rules {{ id step1 }}
The first thing you will want to add to your rules is a line to include the base HUD Map rules next to the Zone rules.

```xml
<Include Path="$(ModelBuilderPath)\Rules\HUDMap.xml"/> <!-- New Inclusion -->
<Include Path="$(ModelBuilderPath)\Rules\Zone.xml"/>
```

## Step 2: Adding a HUD Map file and Mesh {{ id step2 }}
Now that you have the rules, you'll want to add a new [OutputPure3DFile element](/lucasmapbuilder/xml-format/elements/outputs/outputpure3dfile.md) next to your other ones for the HUD map mesh to go into.

You'll also want to add a [Mesh element](/lucasmapbuilder/xml-format/elements/entities/mesh.md). This will be used in the next step.

```xml
<!-- Make sure to change the level number in the file and mesh names to match the level you're building the map for -->
<OutputPure3DFile Name="HUDMap" Path="$(OutputPath)\frontend\scrooby\resource\pure3d\l1hudmap.p3d"/>

<!-- HUD map mesh -->
<Mesh Name="HUDMap">
	<!-- Set which file it goes in and the chunk name -->
    <OutputPure3DFile Name="HUDMap" ChunkName="l1hudmapShape"/>
</Mesh>
```

## Step 3: Updating the ModelOutputInstructions {{ id step3 }}
Next, head down to your `ModelOutputInstructions` named "Zone" and add a line to execute the new rules and one to set the `OutputHUDMapMesh` parameter to the name of the [Mesh element](/lucasmapbuilder/xml-format/elements/entities/mesh.md) you added in the previous step.

```xml
<ModelOutputInstructions Name="Zone">
    <ExecuteInstructions Name="BaseHUDMap"/> <!-- New Instruction -->
    <ExecuteInstructions Name="BaseZone"/> 
    
    <SetParameter Name="OutputHUDMapMesh" Value="HUDMap"/> <!-- New Instruction -->
    <SetParameter Name="VertexColours" Value="World"/>
    <SetParameter Name="FallbackMaterial" Value="Null"/>
</ModelOutputInstructions>
```

## Step 4: Build and check it out ingame {{ id step4 }}
There's no new rules to add for the roads so you're actually already done!

Now it's time to run `Build.bat` to see if it works ingame.

If you've done everything right, the map should successfully build and look something like this:

![final product](/img/lucasmapbuilder/tutorials/map-building/basics/adding-roads/p2_s4_final.png)

# You're done! {{ id end }}
That's it for this tutorial. You're ready to move on to the next one.