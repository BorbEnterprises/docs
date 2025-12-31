---
title: "#1: Making a Basic Map"
description: "This tutorial will guide you through the bare minimum steps to make a basic custom map work in-game."
authors: ["loren"]
---

This tutorial will guide you through the bare minimum steps to make a basic custom map work in-game.

By the end of this tutorial, you should have a small map that is just a square piece of ground with a couple locators.

**NOTE:** Missions will not yet work in this map and it will not have a custom HUD map. This tutorial is just the bare minimum required to go ingame, you will also need to follow the [Adding Roads](adding-roads.md) tutorial after this one for missions to work.

# Prerequisites

{{ snippet lucasmapbuilder/tutorial-prereqs }}

# Part 1: The Mod {{ id part1 }}
To actually play your map in-game, you'll first need a basic mod to start with. We've gone ahead and created a basic mod for these purposes that you can [download here](https://cdn.donutteam.com/AdministratorUploads/DTDocs/LucasMapBuilder/TutorialPackages/MakingABasicMap.zip).

This mod contains the following:

* A basic `Meta.ini` that requires the [Custom Files](/lucasmodlauncher/hacks/cf/intro.md) and [Custom Interior Support](/lucasmodlauncher/hacks/custom-interior-support.md) hacks.
    * Custom Files is, of course, used to allow the mod to provide custom files such as the map itself.
    * Custom Interior Support is used to redefine and remove the Evergreen Terrace interiors from this custom map as they are not applicable to it.
* Level 1 load and initialisation scripts that do the bare minimum required for the map to work.
    * See these scripts for additional details.
* A couple dummy missions with no objectives that will let us jump into our map by creating a new game from the main menu or by selecting Level 1 Mission 1.
* A folder named "_Assets" that you'll use as a working folder for your map.

You will need to install the "Tutorial Map" mod in your copy of the Mod Launcher in order to actually play the map ingame. If you're not sure how to do this, see [Installing Mods](/lucasmodlauncher/mods/installing-mods.md).

Once you have the mod installed, you're ready to get started.

# Part 2: The SketchUp File {{ id part2 }}
## Step 1: Setting up SketchUp {{ id step1 }}
The first thing you will want to do in SketchUp is go to **Window > Preferences** then select **Template** on the left and make sure you're using **Simple Template - Meters**. For all intents and purposes, this tool works in meters so this step is **VERY IMPORTANT** to having numbers in SketchUp and elsewhere line up.

Next, your workspace. SketchUp's workspace is very customizable so, depending on your chosen layout, you may not have certain important panels in view. We'd like to make a couple recommendations for the purposes of these tutorials and creating maps in general.

The Map Builder relies heavily on a hierarchy of groups with special names and tags within their names to understand how to build maps. For this reason we strongly recommend that the **Outliner** is easily accessible. If you don't currently have a tray with the **Outliner** in it, you can go to **Window > New Tray...** to create one containing it. You may also want the **Entity Info** panel in the same tray as it will make editing attributes of the currently selected object easier.

With large models that have many thousands of groups, you may experience slowdown having the **Outliner** open so it may be good to get used to minimizing it by clicking the arrow near its header when you're not using it. It would also be very beneficial to learn and understand how to make use of [Layers](https://help.sketchup.com/en/sketchup/controlling-visibility-layers) for larger map projects.

You will also want the **Materials** and **Components** panels accessible. You can technically put these in the same tray though if you have a good amount of screen real estate or multiple screens, you may find it more productive to make more than one tray and spread them out.

Here's an example workspace:

![example workspace](/img/lucasmapbuilder/tutorials/map-building/basics/making-a-basic-map/p2_s1_exampleworkspace.png)

Lastly, all new SketchUp models begin with a Component named "Chris". You can delete him if you'd like.

## Step 2: Save the model {{ id step2 }}
The first thing you will want to do is save your empty model somewhere. For the purposes of these tutorials, you should save it as "Map.skp" in the "_Assets" folder of the mod you installed in Part 1.

It's also good to try to save fairly often in case something goes wrong (such as a power outage or a SketchUp crash) so you don't lose your work.

## Step 3: Terrain {{ id step3 }}
You'll want to start by making some basic "terrain" in your SketchUp model, for the purposes of this tutorial, try using just a flat rectangle.

You should make this rectangle about 20 meters by 20 meters so there's a good amount of space to walk around.

![flat plane](/img/lucasmapbuilder/tutorials/map-building/basics/making-a-basic-map/p2_s3_rectangle.png)

## Step 4: Setting up the groups {{ id step4 }}
Now that you have some "terrain" you'll want to group it properly so that you can build it into a zone later. Select the square, right click it and click "Make Group". Then double click the group to focus it and repeat this step. This will create a group within that group.

Once you've done that, you should name the outer group to `Zone001` and rename the inner group to `Ground [Intersect]`. Once you've done that, your **Outliner** should look something like this:

![outliner groups](/img/lucasmapbuilder/tutorials/map-building/basics/making-a-basic-map/p2_s4_groups.png)

In this case, the outer group name is something we'll use later on to designate what goes into Zone 1. This means any other entities, groups or components inside this group will get built into that zone's P3D file.

How the actual contents of that group gets processed is fairly simple. By default, everything within this group will become a [Static Entity](/pure3d/chunk-types/chunk-3F00000.md) (a static mesh in the map). From there, special [group tags](../../sketchup-models/group-tags/all-tags.md) can be added to group names to give the tool additional instructions.

In this case, you're using the [Intersect group tag](../../sketchup-models/group-tags/collision/intersect.md) which makes the contents of the group should also get used to create [Intersect collision](/pure3d/chunk-types/chunk-3F00003.md) (the ground). 

[Group tags](../../sketchup-models/group-tags/all-tags.md) are one of the main ways you'll tell the tool how you want the files built and what the groups represent.
 
With those groups setup and named appropriately, you now have the most basic zone possible.

## Step 5: Importing the Locator components {{ id step5 }}
The scripts included in the mod from Part 1 reference a couple locators to specify where the player and their car should start in the level. 

These are also something you're going to create in your SketchUp file using one of the tool's [Special Components](../../sketchup-models/special-components.md).

Go to **File > Import** and navigate to the **Components** folder next to the Map Builder's executable. From there import "Locator.skp" into your model.

This will attach an instance of it on your cursor and you can go ahead and place it down anywhere on your terrain.
   
Now if you go to the **Components** panel and click the little house icon to bring up the list of components in the current model, you should see "Locator" in the list if you imported it correctly.

![components home button](/img/lucasmapbuilder/tutorials/map-building/basics/making-a-basic-map/p2_s5_house.png)

## Step 6: Tagging some Locator components {{ id step6 }}
Now that you've imported and placed a Locator component, select it in the Components list and drag a second one out onto the terrain.

We're going to use these two locators as our player start and car start locators. You'll want to name one of them `level1_homer_start [CarStart]` and name the other one `level1_carstart [CarStart]`. 

The [CarStart group tag](../../sketchup-models/group-tags/locators/carstart.md) used on these components tells the Map Builder to make [Type 3 Car Start locators](/pure3d/chunk-types/chunk-3000005.md#this_types_type3) which, despite their name, are also used as character locators.
   
Now that they're named and tagged select both of the instances, right click and click **Make Group**. Once you've made the group, name it `Level`.

**Make sure this group is in the root of the file and not inside your zone.**

Once you've done that, your **Outliner** should look like this:

![locators in outliner](/img/lucasmapbuilder/tutorials/map-building/basics/making-a-basic-map/p2_s5_outliner.png)

## Step 7: Save again! {{ id step7 }}
Make sure you save everything you've done so far if you haven't already.

# Part 3: Configuring the Map Builder {{ id part3 }}
## Step 1: Creating the build files {{ id step1 }}
To start, you want to create an XML file that will contain all of your rules for the Map Builder and a BAT file to actually launch the tool with your rules.
   
For now, just make a bare bones XML file that just has a [Build](../../xml-format/elements/general/build.md) element inside it. These elements are used as the root of any rules XML file.

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<Build>
	
</Build>
```

Save this file as "Build.xml" into the "_Assets" folder next to your SketchUp file.

Then make a BAT file that launches the Map Builder with "Build.xml" as a command line argument:
```bat
@"C:\path\to\LSHaRMB.exe" "Build.xml"
```

You'll need to manually replace the path with where-ever you put the Map Builder. Save this as "Build.bat" into the same folder when you're done.

Once those are saved, running Build.bat should work and you should get an output that looks something like this:

```text
[12:58:35 PM] MESSAGE: Loading SketchUp SDK DLL (64-bit) 17.0.18899.0...
[12:58:35 PM] MESSAGE: Processing outputs...
[12:58:35 PM] MESSAGE: Processing file outputs...
[12:58:35 PM] SUCCESS: Completed in 25.2060558021864 ms.
```

You haven't told the tool to do anything yet so it hasn't actually created any output files. This is just to make sure that the BAT file is working as intended.

## Step 2: Defining variables {{ id step2 }}
The Map Builder supports defining custom variables and it also has [several predefined variables](../../xml-format/predefined-variables.md) that you'll be using in this tutorial.

Your next order of business is defining a couple of custom variables for the working path and also for where your output files are going to go. You can do this using a [`SetVariable`](../../xml-format/elements/general/setvariable.md) element.

This isn't technically required but its good practice to do.

These can simply go in the root element of the XML file you made in the previous step:
```xml
<!-- Store the folder this XML file is in as the root working path -->
<SetVariable Name="WorkingPath" Value="$(ParentPath)" />

<!-- Get the parent path of our main Rules file then go up a directory then into CustomFiles -->
<SetVariable Name="OutputPath" Value="$(ParentPath)\..\CustomFiles\art" />
```

Notice that `WorkingPath` uses the special predefined `$(ParentPath)` variable. This is so this XML file can store its path and any XML file included by it can use it for paths relative to this file instead of themselves, even if they're in a subfolder.

This tutorial is only going to be using a single custom XML file but this is good practice for more complicated projects.

## Step 3: Including base rules {{ id step3 }}
The Map Builder ships with a number of Rules XML files. These are imperative to getting much of anything done with this tool.

In this case, we're going to be using an [Include element](../../xml-format/elements/general/include.md) to include `Zone.xml` right after the rules defined in the previous step.

```xml
<!-- Use the MapBuilderPath variable to easily fill in the path to the tool's folder -->
<Include Path="$(MapBuilderPath)\Rules\Zone.xml"/>
```

This file gives you access to some [ModelOutputInstructions elements](../../xml-format/elements/outputs/modeloutputinstructions.md) named `BaseZone` and `Locators2` which you will use when writing your own [ModelOutputInstructions](../../xml-format/elements/outputs/modeloutputinstructions.md).

The path above uses the `$(MapBuilderPath)` variable. As you might expect, this is simply the path to where the tool is running from.

## Step 4: Specifying output files and zones {{ id step4 }}
The next step is defining what the output files what output files you're going to be building and where they're going to go. 

For this, you will use a few [OutputPure3DFile elements](../../xml-format/elements/outputs/outputpure3dfile.md).

```xml
<!-- Terra file -->
<OutputPure3DFile Name="Terra" Path="$(OutputPath)\L1_TERRA.p3d"/>

<!-- Zone 1 -->
<OutputPure3DFile Name="Zone001" Path="$(OutputPath)\l1z1.p3d">
    <!-- Tell the tool that this file requires the Terra file to work -->
    <!-- This will also make the tool place textures/shaders used in multiple zones in the Terra file instead of repeating them -->
    <RequiredOutputPure3DFile Name="Terra" Textures="true" Materials="true" Lights="true"/>
</OutputPure3DFile>

<!-- Level Locators -->
<OutputPure3DFile Name="Level" Path="$(OutputPath)\missions\level01\level.p3d" />
```

You'll also need to use a [HitAndRunMap element](../../xml-format/elements/outputs/hitandrunmap.md) to define what file the map's [k-d tree](/pure3d/chunk-types/chunk-3F00004.md) goes in and a couple of [HitAndRunZone elements](../../xml-format/elements/outputs/hitandrunzone.md) that reference it to make the contents of your Terra file and your Zone get counted in the k-d tree.

```xml
<!-- Define the map -->
<!-- 	This gives you control what file the k-d tree goes in, the size of its tree nodes and how many DynaPhys are allowed in each node -->
<HitAndRunMap Name="Map" TreeMinimumNodeSizeX="20" TreeMinimumNodeSizeZ="20" TreeDynaPhysEntityLimit="10">
    <OutputPure3DFile Name="Terra"/>
</HitAndRunMap>

<!-- Define zone info -->
<!-- 	While things can be outputted directly into Pure3D files, these elements make things get counted in the k-d tree -->
<!-- 	Which is VERY important -->
<!-- 	This is not required for the level locators file since its just locators which aren't counted in the tree -->
<HitAndRunZone Name="Terra" Map="Map">
    <OutputPure3DFile Name="Terra"/>
</HitAndRunZone>
<HitAndRunZone Name="Zone001" Map="Map">
    <OutputPure3DFile Name="Zone001"/>
</HitAndRunZone>
```

With these rules in place, running the tool should now build (mostly) empty P3D files to the specified paths.

## Step 5: Making a light group and vertex colors {{ id step5 }}
Next, you should specify some basic lighting rules.

For this, you'll need a [LightGroup element](../../xml-format/elements/lighting/lightgroup.md) and a [VertexColours element](../../xml-format/elements/lighting/vertexcolours.md). 

The former is used to create [Light Groups](/pure3d/chunk-types/chunk-2380) and they can also be referenced by the latter which can referenced later on to apply the light sources to map models as vertex colours.

```xml
<!-- Specify the Light Group and name it -->
<LightGroup Name="Level1">
    <!-- These lights are more or less equivalent to the "sun" light group in the original game's L1_TERRA -->
    <AmbientLight Name="Ss_ambientLightShape1" Red="89" Green="89" Blue="89"/>
    <DirectionalLight Name="Simpsons_sun_directionalShape3" Red="89" Green="89" Blue="89" DirectionX="0" DirectionY="-0.5" DirectionZ="-0.866"/>
    <DirectionalLight Name="Simpsons_sun_directionalShape2" Red="140" Green="140" Blue="140" DirectionX="-0.75" DirectionY="-0.5" DirectionZ="0.433"/>
    <DirectionalLight Name="Simpsons_sun_directionalShape4" Red="140" Green="140" Blue="140" DirectionX="0.75" DirectionY="-0.5" DirectionZ="0.433"/>
    
    <!-- Specify an output file and chunk name to build this group into -->
	<!-- This is not technically required but is recommended if you're not getting a light group from somewhere else -->
    <OutputPure3DFile Name="Terra" ChunkName="sun"/>
</LightGroup>

<!-- Specify VertexColours rules that reference that light group -->
<!-- You'll reference these later on in Step 8 -->
<VertexColours Name="World" Light="Level1" LightAbsolute="true"/>
```

## Step 6: Defining a basic material {{ id step6 }}
While you can use materials in SketchUp to apply textures to surfaces in your map, you haven't done that yet (if you've been following this tutorial closely, at least).

With that in mind, you should define a basic colored material in XML instead with a [Material element](../../xml-format/elements/materials/material.md). 

```xml
<!-- Basic solid white material -->
<!-- You'll reference this later on in Step 8 -->
<Material Name="Null" Red="255" Green="255" Blue="255"/>
```

## Step 7: Specifying input files {{ id step7 }}
Next up, you'll want to tell the tool what your input files are.

This is done with [InputSketchUpModel elements](../../xml-format/elements/inputs/inputsketchupmodel.md) for SKP files and [InputPure3DFile elements](../../xml-format/elements/inputs/inputpure3dfile.md) for Pure3D files.

```xml
<!-- Of course you want to input your Map's SketchUp file -->
<!-- Here we use the WorkingPath variable we set earlier -->
<InputSketchUpModel Name="Map" Path="$(WorkingPath)\Map.skp"/>

<!-- You'll also want to input a couple files from the original game -->
<!-- You'll use these later on in Step 9 -->
<InputPure3DFile Name="L1_Terra" Path="$(GamePath)\art\L1_TERRA.p3d" />
<InputPure3DFile Name="L1_Level" Path="$(GamePath)\art\missions\level01\level.p3d" />
```

## Step 8: Defining model output instructions {{ id step8 }}
Now you're finally at the step where you tell the tool how to handle your SketchUp model.

This is done using [ModelOutputInstructions elements](../../xml-format/elements/outputs/modeloutputinstructions.md) and a [SketchUpModelOutput element](../../xml-format/elements/outputs/sketchupmodeloutput.md)

```xml
<!-- Instruction set used for each zone -->
<!-- 	Defined here so it can be used multiple times in the SketchUpModelOutput -->
<ModelOutputInstructions Name="Zone">
    <!-- Execute the BaseZone instructions we included from "Zone.xml" in Step 3 -->
    <ExecuteInstructions Name="BaseZone"/>
    
    <!-- Set the VertexColours parameter to the one defined in Step 5 -->
    <SetParameter Name="VertexColours" Value="World"/>
    
    <!-- Set the FallbackMaterial parameter to the "Null" material created in Step 6 -->
    <SetParameter Name="FallbackMaterial" Value="Null"/>
</ModelOutputInstructions>

<!-- Main instruction set -->
<!-- 	Execute all of these instructions on the InputSketchUpModel named "Map" -->
<SketchUpModelOutput InputSketchUpModel="Map">

    <!-- Add selectors for each group name -->
    <!-- Basically when that group name is encountered, the tool will execute the instructions inside the selector -->
	<!-- "Exclusive" makes it so the selected group will only have these instructions applied to it -->

    <AddSelector Pattern="^Terra$" Exclusive="true">
        <!-- The Terra file and each zone must use AddOutputZone to output to the HitAndRunZones defined in Step 4 -->
        <AddOutputZone Name="Terra"/>
        
        <!-- Execute the instruction set you defined above -->
        <ExecuteInstructions Name="Zone"/>
    </AddSelector>
    
    <AddSelector Pattern="^Zone001$" Exclusive="true">
        <AddOutputZone Name="Zone001"/>
        <ExecuteInstructions Name="Zone"/>
    </AddSelector>
    
    <AddSelector Pattern="^Level$" Exclusive="true">
        <!-- Output directly to an OutputPure3DFile instead of a HitAndRunZone -->
        <AddOutputPure3DFile Name="Level"/>
        
        <!-- Use "Locators2" instead for groups that only contain locators -->
        <ExecuteInstructions Name="Locators2"/>
    </AddSelector>
</SketchUpModelOutput>
```

## Step 9: Borrowing from the original game {{ id step9 }}
You're almost done. All you need to do now is extract a few things from the base game that are required for your map to work.

For this step, you'll be using the base game files you inputted in Step 7 with some [Pure3DFileChunksOutput elements](../../xml-format/elements/outputs/pure3dfilechunksoutput.md).

```xml
<!-- "EnvMap.bmp" is being copied from Input "L1_TERRA" P3D into our new Output "Terra" P3D file so car reflections work -->
<!-- 	This is placed at the start of the Terra file with Start="true" -->
<Pure3DFileChunksOutput OutputPure3DFile="Terra" InputPure3DFile="L1_Terra" Type="Texture" Name="EnvMap.bmp" Start="true"/>

<!-- Input Road Arrow Anims -->
<!-- 	This is REQUIRED for missions to work (though your map doesn't have any roads so they won't work yet for that reason) -->
<!-- 	These need to be placed after any Intersections in the Terra file so you need to specify AfterIntersections="true" -->
<!-- 	For that same reason, it is crucial that this is after your SketchUpModelOutput element -->
<Pure3DFileChunksOutput OutputPure3DFile="Terra" InputPure3DFile="L1_Terra" Type="Anim" Name="darrow" AfterIntersections="true"/>
<Pure3DFileChunksOutput OutputPure3DFile="Terra" InputPure3DFile="L1_Terra" Type="Anim" Name="warrow" AfterIntersections="true"/>

<!-- "coinShape_000" is being copied from the Input "L1_Level" P3D to the new Output "Level" P3D -->
<!-- 	Since this is just a mesh, you can really put it wherever you want as long as level.mfk loads it -->
<!--	level.p3d is just where Radical put theirs -->
<Pure3DFileChunksOutput OutputPure3DFile="Level" InputPure3DFile="L1_Level" Type="Mesh" Name="coinShape_000"/>
```

## Step 10: Build and check it out ingame {{ id step10 }}
Now it's time to run Build.bat again to see if it works ingame.

If you've done everything right, the map should successfully build and look something like this.

![final product](/img/lucasmapbuilder/tutorials/map-building/basics/making-a-basic-map/p3_s10_final.png)

# You're done! {{ id end }}
That's it for this tutorial. You're ready to move on to the next one.