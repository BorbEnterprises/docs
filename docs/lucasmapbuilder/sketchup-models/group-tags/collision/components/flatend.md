---
title: FlatEnd
description: "This tag makes a CollisionCylinder component build a Collision Cylinder with flat ends instead of rounded ones."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag makes a CollisionCylinder component build a Collision Cylinder with flat ends instead of rounded ones.

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
GroupName [FlatEnd]
```

# Group Structure
This tag should be applied directly to a [CollisionCylinder Component](../../../special-components.md#collisioncylinder).

# Examples
TODO

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.