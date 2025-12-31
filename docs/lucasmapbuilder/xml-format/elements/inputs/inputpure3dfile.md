---
title: InputPure3DFile
description: This element is used to input a Pure3D File.
summary:
    initialVersion: "1.0"
---

# This Element
This element is used to input a Pure3D File.

```xml
<InputPure3DFile Name="L1_TERRA" Path="$(GamePath)\L1_TERRA.p3d">
	<!-- See Child Elements -->
</InputPure3DFile>
```

* **Name**: The name to reference this input file from elsewhere.
* **Path**: The path to the file.

# Child Elements
## RequiredInputPure3DFile
This element allows you to specify another InputPure3DFile whose contents are required for this one. This is useful when inputting individual zones from the original game or other files that reference external chunks.

```xml
<InputPure3DFile Name="L1_TERRA" Path="$(GamePath)\L1_TERRA.p3d" />

<InputPure3DFile Name="L1Z1" Path="$(GamePath)\l1z1.p3d">
	<RequiredInputPure3DFile Name="L1_TERRA" />
</InputPure3DFile>
```

* **Name**: The name of the InputPure3DFile that's required for this one.

# Version History
## 1.0
Initial release.