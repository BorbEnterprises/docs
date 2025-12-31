---
title: Gag
# description: ""
summary:
    initialVersion: "1.0"
---

# This Element
This element is used to define information about gags.

```xml
<Gag Name="Chalkboard" Animation="Gag_Chalkboard" Cyclic="false">
	<!-- See Child Elements -->
</Gag>
```

* **Name**: The name of the gag.
* **Animation**: The name of a [PoseTransformAnimation](../animations/posetransformanimation.md) to use on this gag.
* **Cyclic**: TODO.

# Child Elements
## OutputPure3DFile
This element is used to output the gag to an [OutputPure3DFile](../outputs/outputpure3dfile.md).

```xml
<OutputPure3DFile Name="MyOutputFile" />
```

* **Name**: The name of the [OutputPure3DFile](../outputs/outputpure3dfile.md) to put the gag in.

# Notes
Building gags will cause the tool to output a file called `GagLocators.txt` containing the locations of every gag for use in the [GagSetPosition](/hitandrun/scripting/mfk-commands/gagsetposition.md).

# Version History
## 1.0
Initial release.