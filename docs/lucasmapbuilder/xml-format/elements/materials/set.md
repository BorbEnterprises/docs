---
title: Set
description: "This element can be used to create a Set chunk in an output P3D file."
summary:
    initialVersion: "1.0"
---

# This Element
This element can be used to create a [Set](../../../../pure3d/chunk-types/chunk-3000110.md) chunk in an output P3D file.

```xml
<Set Name="SpringfieldXSigns">
    <!-- Textures go here -->
</Set>
```

* **Name**: The name of the set to be referenced elsewhere such as in [`Parameter`](materialrules.md#parameter) elements in [`MaterialRules`](materialrules.md).

# Child: Textures
This element sets a path to a folder containing the textures to use in the set.

```xml
<Set Name="SpringfieldXSigns">
    <Textures Path="$(LocalResourcesPath)\Textures\Sets\SpringfieldXSigns"/>
</Set>
```

* **Path**: The path to a folder containing images to put in the set.
    * These images must have a width and height that are powers of two (32x32, 64x32, 128x256, etc.).

# Version History
## 1.0
Initial release.