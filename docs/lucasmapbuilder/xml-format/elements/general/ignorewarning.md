---
title: IgnoreWarning
description: "This type of element allows you to hide specific types of warnings. This is useful if you're intentionally doing something that would be invalid under normal circumstances but is not in your case."
summary:
    initialVersion: "1.0"
---

# This Element
This type of element allows you to hide specific types of warnings. This is useful if you're intentionally doing something that would be invalid under normal circumstances but is not in your case.

```xml
<!-- For example, DM4 map extensions have new roads that are not connected -->
<!-- This is fine though because these roads get added to Radical's existing road network -->
<!-- Therefore we ignore the warning  -->
<IgnoredWarning Name="RoadNetworkMultiple"/>
```

* **Name**: The name of the warning type to ignore.
    * **CollisionShapeNotInPhys**: Disables the warnings shown when a Collision component is not in any type of Phys structure.
    * **FacesBackMaterialIgnoring**: TODO
    * **FacesBackMaterialUsing**: TODO
    * **FacesNoMaterial**: Disables the warnings shown when an input SketchUp file has faces with no materials on them.
    * **IgnoringAnimDynaPhys**: TODO
    * **IgnoringAnimObj**: TODO
    * **IntersectTriangleNormalZero**: TODO
    * **IntersectTriangleSideways**: TODO
    * **IntersectTriangleUpsideDown**: TODO
    * **IntersectionDuplicateName**: TODO
    * **IntersectionNoRoads**: TODO
    * **IntersectionNotInTerraFile**: Disables the warnings shown when an [Intersection](../../../../pure3d/chunk-types/chunk-3000004.md) is not built into a Terra file.
    * **MissingGag**: TODO
    * **PathPositionsTooMany**: TODO
    * **RoadNetworkMultiple**: Disables the warning shown when there are multiple road networks built.
    * **RoadSideNotInIntersectionBothSides**: TODO
    * **RoadSideNotInIntersectionOneSide**: TODO

# Child Elements
This type of element has no children.

# Version History
## 1.0
Initial release.