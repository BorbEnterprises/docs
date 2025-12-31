---
title: InputSketchUpModel
description: This type of element allows you to define a SketchUp model as an input file.
summary:
    initialVersion: "1.0"
---

# This Element
This type of element allows you to define a SketchUp model as an input file.

```xml
<InputSketchUpModel Name="IndustrialZone" Path="$(LocalResourcesPath)\SketchUpModels\IndustrialZone5.skp" MaterialRules="World"/>
```

* **Name**: The name of the model that is used when referencing it elsewhere.
* **Path**: The path to the SKP file.
* **MaterialRules**: The [`MaterialRules`](../materials/materialrules.md) to use when processing this model's materials.
    * Optional.

# Child Elements
This type of element has no children.

# Version History
## 1.0
Initial release.