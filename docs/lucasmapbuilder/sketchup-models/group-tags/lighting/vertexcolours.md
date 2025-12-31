---
title: VertexColours
description: "This tag applies a VertexColours XML Element to the contents of the group it is applied to."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag applies a [VertexColours XML Element](../../../xml-format/elements/lighting/vertexcolours.md) to the contents of the group it is applied to.

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `StateProp.xml`
* `Vehicle.xml`
* `Zone.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

* `BaseZone`
    * Only when including `Zone.xml`.
* `StateProp`
    * Only when including `StateProp.xml`.
* `Vehicle`
    * Only when including `Vehicle.xml`.

# Syntax
```text
Name [VertexColours] [<VertexColours>]
```

* **VertexColours**: The name of the [VertexColours XML Element](../../../xml-format/elements/lighting/vertexcolours.md) to apply to this group.

# Group Structure
This tag can be applied to any group.

# Examples
TODO

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.