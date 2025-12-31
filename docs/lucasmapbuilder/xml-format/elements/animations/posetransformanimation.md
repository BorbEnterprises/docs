---
title: PoseTransformAnimation
description: "This type of element is used to create pose transform (PTRN) type Animations."
summary:
    initialVersion: "1.0"
---

# This Element {{ id this }}
This type of element is used to create pose transform (PTRN) type [Animations](/pure3d/chunk-types/chunk-121000.md#this_values_animation-type).

These are referenced by various [group tags](/lucasmapbuilder/sketchup-models/group-tags/all-tags.md) such as the [Anim group tag](/lucasmapbuilder/sketchup-models/group-tags/entities/anim.md).

```xml
<PoseTransformAnimation Name="MyAnimation" NumFrames="120" FrameRate="60">
	<!-- See Child Elements -->
</PoseTransformAnimation>
```

* **Name**: The name of the animation to reference it by elsewhere.
* **NumFrames**: The total number of frames in the animation.
* **FrameRate**: The number of frames that will be played per second.

# Child Elements {{ id children }}
## Group
This type of element represents an [Animation Group](/pure3d/chunk-types/chunk-121000#children_animation-group-(0x121001)).

This type of element can be repeated multiple times.

```xml
<Group Name="MyGroup">
	<!-- See RotationChannel and TranslationChannel -->
</Group>
```

* **Name** The name of this group.

## RotationChannel
This type of element represents a [Quaternion Channel](/pure3d/chunk-types/chunk-121000.md#children_121105) with simpler to edit values.

```xml
<RotationChannel>
	<!-- See RotationAxisValue -->
</RotationChannel>
```

## RotationAxisValue
This type of element represents a value with [TranslationChannel](#children_rotationchannel) elements.

```xml
<RotationAxisValue Frame="0" AxisX="0" AxisY="1" AxisZ="0" Angle="0" Relative="true" />
```

* **Frame**: The frame index this value applies on.
* **AxisX**: Set whether or not this value applies to the X axis.
* **AxisY**: Set whether or not this value applies to the Y axis.
* **AxisZ**: Set whether or not this value applies to the Z axis.
* **Angle**: Set the angle of the affected axes.
* **Relative**: Set whether or not this animation frame is relative to the base position.

## TranslationChannel
This type of element represents a [Vector 3D OF Channel](/pure3d/chunk-types/chunk-121000.md#children_121104).

```xml
<TranslationChannel>
	<!-- See Value -->
</TranslationChannel>
```

## Value
This type of element represents a value with [TranslationChannel](#children_translationchannel) elements.

```xml
<Value Frame="0" X="0" Y="0" Z="0" Relative="true" />
```

* **Frame**: The frame index this value applies on.
* **X**: The X value on that Frame.
* **Y**: The Y value on that Frame.
* **Z**: The Z value on that Frame.
* **Relative**: Set whether or not this animation frame is relative to the base position.

# Examples
This is a full example animation for the lights on a police car:

```xml
<PoseTransformAnimation Name="PoliceCar" NumFrames="45" FrameRate="45">
	<Group Name="Car">
		<TranslationChannel>
			<!-- This example is for demonstration purposes -->
			<!-- Actually having the car go up and down would be a bit silly -->
			<Value Frame="0" X="0" Y="0" Z="0" Relative="true" />
			<Value Frame="28" X="0" Y="5" Z="0" Relative="true" />
			<Value Frame="45" X="0" Y="0" Z="0" Relative="true" />
		</TranslationChannel>
	</Group>
	<Group Name="SirenLarge">
		<RotationChannel>
			<RotationAxisValue Frame="0" AxisX="0" AxisY="1" AxisZ="0" Angle="0" Relative="true" />
			<RotationAxisValue Frame="15" AxisX="0" AxisY="1" AxisZ="0" Angle="120" Relative="true" />
			<RotationAxisValue Frame="30" AxisX="0" AxisY="1" AxisZ="0" Angle="240" Relative="true" />
			<RotationAxisValue Frame="45" AxisX="0" AxisY="1" AxisZ="0" Angle="360" Relative="true" />
		</RotationChannel>
	</Group>
	<Group Name="SirenLargeReverse">
		<RotationChannel>
			<RotationAxisValue Frame="0" AxisX="0" AxisY="1" AxisZ="0" Angle="0" Relative="true" />
			<RotationAxisValue Frame="15" AxisX="0" AxisY="1" AxisZ="0" Angle="-120" Relative="true" />
			<RotationAxisValue Frame="30" AxisX="0" AxisY="1" AxisZ="0" Angle="-240" Relative="true" />
			<RotationAxisValue Frame="45" AxisX="0" AxisY="1" AxisZ="0" Angle="-360" Relative="true" />
		</RotationChannel>
	</Group>
</PoseTransformAnimation>
```

This is how this animation would be referenced with the [Anim group tag](/lucasmapbuilder/sketchup-models/group-tags/entities/anim.md):

![pose transform animation used in anim group tag example](/img/lucasmapbuilder/sketchup-models/group-tags/entities/anim_example.png)

# Version History
## 1.0
Initial release.