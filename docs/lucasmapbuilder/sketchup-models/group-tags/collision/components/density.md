---
title: Density
description: "This tag sets the density of a specific collision component."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag sets the density of a specific collision component.

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
GroupName [Density] [<Density>]
```

* **Density**: The density of the collision.

# Group Structure
This tag should be applied directly to a [CollisionBox Component](../../../special-components.md#collisionbox), a [CollisionCylinder Component](../../../special-components.md#collisioncylinder) or a [CollisionSphere Component](../../../special-components.md#collisionsphere), 

# Examples
TODO

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.