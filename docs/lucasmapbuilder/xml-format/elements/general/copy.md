---
title: Copy
description: "This element can be used to copy files as part of the build process."
summary:
	initialVersion: "1.0"
---

# This Element
This element can be used to copy files as part of the build process.

```xml
<Copy SourcePath="$(Example)\Source\File.p3d" DestinationPath="$(Example)\Target\File.p3d" />
```

* **SourcePath**: The source file path to copy from.
* **DestinationPath**: The source file path to copy to.
	* This will replace the file at the destination path, if it already exists.

# Child Elements
This type of element has no children.

# Version History
## 1.0
Initial release.