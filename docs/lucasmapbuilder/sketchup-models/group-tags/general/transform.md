---
title: Transform
description: "This tag applies a Transform XML Element to the contents of the group it's applied to."
summary:
    initialVersion: "1.0"
---

This tag applies a Transform XML Element to the contents of the group it's applied to.

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `HUDMap.xml`
* `StateProp.xml`
* `Vehicle.xml`
* `Zone.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

{{ snippet lucasmapbuilder/sketchup-models/group-tags/flipfaces-transform-instructions }}

# Syntax
```
GroupName [Transform] [<TransformName>]
```

* **TransformName**: The name of a [Transform XML Element](../../../xml-format/elements/general/transform.md) to apply to the contents of the group.

# Group Structure
This tag can be applied to any group.

# Examples
This is an example of a group with this tag applied to it:

![transform example](/img/lucasmapbuilder/sketchup-models/group-tags/general/transform-example.png)

This tag requires you to define a [Transform XML Element](../../../xml-format/elements/general/transform.md) somewhere in your XML rules.

```xml
<!-- Example -->
<Transform Name="Tall">
    <Scaling Y="4.0">
</Transform>
```

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.