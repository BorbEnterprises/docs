---
title: Transform
description: "This type of element allows you to define transformations that can be applied to groups in SketchUp models via the Transform group tag."
summary:
    initialVersion: "1.0"
---

# This Element
This type of element allows you to define transformations that can be applied to groups in SketchUp models via the [Transform Group Tag](../../../sketchup-models/group-tags/general/transform.md).

```xml
<Transform Name="MyTransform">
    <!-- See Child Elements -->
</Transform>
```

* **Name**: The name of the transform.

# Child: Scaling
This element allows you to scale the group.

```xml
<Transform Name="UniformScalingExample">
    <!-- Scale the group by 2 on all axes -->
    <Scaling Value="2.0">
</Transform>

<Transform>
    <!-- Scale the group on individual axes -->
    <Scaling X="2.0" Y="1.5" Z="3.0">
</Transform>
```

**Uniform Scaling**

* **Value**: The amount to scale the group by on every axis.

**Individual Axis Scaling**

* **X**: The amount to scale the group by on the X axis.
* **Y**: The amount to scale the group by on the Y axis.
* **Z**: The amount to scale the group by on the Z axis.

# Child: Translation
This element allows you to translate the position of the group.

```xml
<Transform Name="TranslationExample">
    <!-- Translate everything 10 meters on each axis -->
    <Translate X="10.0" Y="10.0" Z="10.0">
</Transform>
```

* **X**: The amount of meters to translate the group by on the X axis.
* **Y**: The amount of meters to translate the group by on the Y axis.
* **Z**: The amount of meters to translate the group by on the Z axis.

# Child: RotationX / RotationY / RotationZ
These elements allow you to rotate the group along each axis.

```xml
<Transform Name="RotationExample">
    <!-- Rotate 45 degrees along each axis -->
    <RotationX Value="45">
    <RotationY Value="45">
    <RotationZ Value="45">
</Transform>
```

* **Value**: The amount of degrees to rotate the group by on the given axis.

# Child: Transform
These elements allow you to nest transforms inside each other.

```xml
<Transform Name="BaseTransform">
	<!-- ... -->
</Transform>

<Transform Name="SubTransformExample">
	<Transform Name="BaseTransform" />
</Transform>
```

# Notes
The various child tags can be used with one another.

# Version History
## 1.0
Initial release.