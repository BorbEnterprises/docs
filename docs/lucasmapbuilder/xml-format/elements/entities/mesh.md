---
title: Mesh
description: "This element is used to create a Mesh."
summary:
    initialVersion: "1.0"
---

# This Element
This element is used to create a [Mesh](../../../../pure3d/chunk-types/chunk-10000.md).

```xml
<Mesh Name="HUDMap">
	<!-- See Child Elements -->
</Mesh>
```

* **Name**: The name used to reference this Mesh element elsewhere.

# Child Elements
## OutputPure3DFile
This element is used to output the [Mesh](../../../../pure3d/chunk-types/chunk-10000.md) to an [OutputPure3DFile](../outputs/outputpure3dfile.md).

```xml
<OutputPure3DFile Name="MyOutputFile" ChunkName="myLightGroup" />
```

* **Name**: The name of the [OutputPure3DFile](../outputs/outputpure3dfile.md) to put the [Mesh Chunk](../../../../pure3d/chunk-types/chunk-10000.md) in.
* **ChunkName**: The name of the [Mesh Chunk](../../../../pure3d/chunk-types/chunk-10000.md).

# Version History
## 1.0
Initial release.