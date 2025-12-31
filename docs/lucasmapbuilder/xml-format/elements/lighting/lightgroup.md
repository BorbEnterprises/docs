---
title: LightGroup
#description: TODO
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

# This Element
This type of element is used to apply vertex colours to output models and can also be used create [Light Group Chunks](../../../../pure3d/chunk-types/chunk-2380.md) in an [OutputPure3DFile](../outputs/outputpure3dfile.md).

```xml
<LightGroup Name="World">
	<!-- See Child Elements -->
</LightGroup>
```

* **Name**: The name used to reference this LightGroup elsewhere.

# Child Elements
## AmbientLight
TODO

## DirectionalLight
TODO

## Light
TODO

## OutputPure3DFile
This element is used to create a [Light Group Chunk](../../../../pure3d/chunk-types/chunk-2380.md) in an [OutputPure3DFile](../outputs/outputpure3dfile.md).

```xml
<OutputPure3DFile Name="MyOutputFile" ChunkName="myLightGroup" />
```

* **Name**: The name of the [OutputPure3DFile](../outputs/outputpure3dfile.md) to put the [Light Group Chunk](../../../../pure3d/chunk-types/chunk-2380.md) in.
* **ChunkName**: The name of the [Light Group Chunk](../../../../pure3d/chunk-types/chunk-2380.md).

# Version History
## 1.0
Initial release.