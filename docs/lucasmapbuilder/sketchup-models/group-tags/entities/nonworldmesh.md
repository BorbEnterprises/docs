---
title: NonWorldMesh
description: "This tag makes it so nothing in the group it is applied to will be built as static entities or other types of visible entities in the world."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag makes it so nothing in the group it is applied to will be built as static entities or other types of visible entities in the world.

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
Name [NonWorldMesh]
```

# Group Structure
This tag can be applied to any group.

# Examples
TODO

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.