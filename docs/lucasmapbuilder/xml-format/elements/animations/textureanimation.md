---
title: TextureAnimation
description: "This element is used to create a texture animation for a material."
summary:
    initialVersion: "1.0"
---

# This Element {{ id this }}
This element is used to create a texture animation for a material. 

These can be referenced by a [MaterialRules Parameter](../materials/materialrules.md#children_parameter).

```xml
<TextureAnimation Name="Water" FrameRate="20">
    <!-- See Child Elements -->
</TextureAnimation>
```

* **Name**: The name of the animation to be referenced elsewhere.
* **FrameRate**: The amount of frames of this animation that will be played in a second.

> *OR*

* **Interval**: The amount of time between frames in milliseconds.

# Child Elements {{ id children }}
## Frame
This element is used to define a frame used in the animation.

```xml
<TextureAnimation Name="Water" Interval="100">
	<Frame Path="water1.png" />
	<Frame Path="water2.png" />
	<Frame Path="water3.png" />
	...
	<Frame Path="water14.png" />
	<Frame Path="water15.png" />
	<Frame Path="water16.png" />
</TextureAnimation>
```

* **Path**: The path to the image to use for this frame.

## Frames
This element is used to define the frames used in the animation.

```xml
<TextureAnimation Name="Water" FrameRate="10">
    <Frames PathPrefix="water" PathSuffix=".png" IndexStart="1" IndexEnd="16" IndexStep="1"/>
</TextureAnimation>
```

* **PathPrefix**: The prefix of the path.
* **PathSuffix**: The suffix of the path.
* **IndexStart**: The start index for the frames.
* **IndexEnd**: The end index for the frames.
* **IndexStep**: The step to use when interating the frames.

`PathPrefix` and `PathSuffix` are concatenated together with an index in between them for each frame. This needs to be reflected in the file names.

To convey this better, here's an example of the folder of textures defined above:

![textureanimation frames example](/img/lucasmapbuilder/miscellaneous/textureanimation_frames_example.png)

## ColourFrames
This element is used to generate 1 pixel by 1 pixel colored textures easing from the start color to the end color.

```xml
<TextureAnimation Name="ColourExample" FrameRate="10">
	<!-- Generate 20 frames going from full blue to full green -->
	<ColourFrames StartRed="0" StartGreen="0" StartBlue="255" EndRed="0" EndGreen="255" EndBlue="0" Count="20" />

	<!-- Generate 20 frames going back the other way -->
	<ColourFrames StartRed="0" StartGreen="255" StartBlue="0" EndRed="0" EndGreen="0" EndBlue="255" Count="20" />
</TextureAnimation>
```

* **StartRed**: The starting red value.
* **StartGreen**: The starting green value.
* **StartBlue**: The starting blue value.
* **EndRed**: The end red value.
* **EndGreen**: The end green value.
* **EndBlue**: The end blue value.

# Example
This is an example that makes a TV static material animated:

```xml
<TextureAnimation Name="TVStatic" FrameRate="20">
	<Frames PathPrefix="$(LocalResourcesPath)\Textures\Animations\TVStatic\tvstatic" PathSuffix=".png" IndexStart="1" IndexEnd="11" IndexStep="1"/>
</TextureAnimation>

<MaterialRules Name="World">
	<Selector Pattern="^tvstatic$" Exclusive="true">
		<Parameter Name="Animation" Value="TVStatic"/>
	</Selector>
</MaterialRules>
```

# Version History
## 1.0
Initial release.