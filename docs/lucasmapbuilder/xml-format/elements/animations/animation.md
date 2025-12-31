---
title: Animation
description: "This type of element is used to create Animations."
summary:
	initialVersion: "1.0"
---

# This Element {{ id this }}
This type of element is used to create [Animations](/pure3d/chunk-types/chunk-121000.md#this_values_animation-type). These are basically 1:1 representations of those chunks but in XML form.

```xml
<Animation Name="MyAnimation" Type="BQG" NumFrames="120" FrameRate="60" Cyclic="0">
	<!-- See Child Elements -->
</Animation>
```

* **Name**: The name of this animation to reference it by elsewhere.
* **Type**: The type of this animation.
	* See [Animation (0x121000)](/pure3d/chunk-types/chunk-121000.md#this_values_animation-type).
* **NumFrames**: The total number of frames in the animation.
* **FrameRate**: The number of frames that will be played per second.
* **Cyclic**: Whether or not the animation is cyclic.

# Child Elements {{ id children }}
## Group
This type of element represents an [Animation Group](/pure3d/chunk-types/chunk-121000.md#children_121001).

This type of element can be repeated multiple times.

```xml
<Group Name="MyGroup">
	<!-- See QuaternionChannel, VectorChannel, Float1Channel, Float2Channel, BooleanChannel, ColourChannel and EntityChannel -->
</Group>
```

* **Name** The name of this group.

## QuaternionChannel
This type of element represents a [Quaternion Channel](/pure3d/chunk-types/chunk-121000.md#children_121105).

```xml
<QuaternionChannel Parameter="ROT">
	<!-- See Value -->
</QuaternionChannel>
```

* **Parameter**: Specifies the parameter on the channel.

## VectorChannel
This type of element represents a [Vector 3D OF Channel](/pure3d/chunk-types/chunk-121000.md#children_121104).

```xml
<VectorChannel Parameter="TRAN">
	<!-- See Value -->
</VectorChannel>
```

* **Parameter**: Specifies the parameter on the channel.

## Float1Channel
This type of element represents a [Float 1 Channel](/pure3d/chunk-types/chunk-121000.md#children_121100).

```xml
<Float1Channel Parameter="DIST">
	<!-- See Value -->
</Float1Channel>
```

* **Parameter**: Specifies the parameter on the channel.

## Float2Channel
This type of element represents a [Float 2 Channel](/pure3d/chunk-types/chunk-121000.md#children_121101).

```xml
<Float2Channel Parameter="DIST">
	<!-- See Value -->
</Float2Channel>
```

* **Parameter**: Specifies the parameter on the channel.

## BooleanChannel
This type of element represents a [Boolean Channel](/pure3d/chunk-types/chunk-121000.md#children_121108).

```xml
<BooleanChannel Parameter="VIS" StartState="false">
	<!-- See Value -->
</BooleanChannel>
```

* **Parameter**: Specifies the parameter on the channel.

## ColourChannel
This type of element represents a [Colour Channel](/pure3d/chunk-types/chunk-121000.md#children_121109).

```xml
<BooleanChannel Parameter="CLR">
	<!-- See Value -->
</BooleanChannel>
```

* **Parameter**: Specifies the parameter on the channel.

## EntityChannel
This type of element represents an [Entity Channel](/pure3d/chunk-types/chunk-121000.md#children_121107).

```xml
<EntityChannel Parameter="TEX">
	<!-- See Value -->
</EntityChannel>
```

## Value
This type of element represents a value within the aforementioned types of animation channels.

{{ tabs }}
{{ tab QuaternionChannel }}

```xml
<Value Frame="0" X="0.707106769" Y="0" Z="0" W="0.707106769" />
```

* **Frame**: The frame index this value applies on.
* **X**: The X value of the quaternion on that Frame.
* **Y**: The Y value of the quaternion on that Frame.
* **Z**: The Z value of the quaternion on that Frame.
* **W**: The W value of the quaternion on that Frame.

{{ endtab }}
{{ tab VectorChannel }}

```xml
<Value Frame="0" X="0" Y="0" Z="0" />
```

* **Frame**: The frame index this value applies on.
* **X**: The X value of the vector on that Frame.
* **Y**: The Y value of the vector on that Frame.
* **Z**: The Z value of the vector on that Frame.

{{ endtab }}
{{ tab Float1Channel }}

```xml
<Value Frame="0" Value="1.201405" />
```

* **Frame**: The frame index this value applies on.
* **Value**: The value of the float on that Frame.

{{ endtab }}
{{ tab Float2Channel }}

```xml
<Value Frame="0" X="0" Y="0" />
```

* **Frame**: The frame index this value applies on.
* **X**: The X value of the float on that Frame.
* **Y**: The Y value of the float on that Frame.

{{ endtab }}
{{ tab BooleanChannel }}

```xml
<Value Frame="0" />
```

* **Frame**: The frame index the boolean alternates on.

{{ endtab }}
{{ tab ColourChannel }}

```xml
<Value Frame="0" Red="255" Green="255" Blue="255" Alpha="255" />
```

* **Frame**: The frame index this value applies on.
* **Red**: The red value for this Frame.
* **Green**: The green value for this Frame.
* **Blue**: The blue value for this Frame.
* **Alpha**: The alpha value for this Frame.

{{ endtab }}
{{ tab EntityChannel }}

```xml
<Value Frame="0" Value="l2r3river.bmp.1" />
```

* **Frame**: The frame index this texture applies on.
* **Value**: The texture name to use for this frame.

{{ endtab }}
{{ endtabs }}

# Examples
TODO

# Version History
## 1.0
Initial release.