---
title: StaticPhys
description: "This tag is used to create Static Phys Chunks. These chunks are static collision in the world made up of boxes, cylinders and spheres."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag is used to create [Static Phys Chunks](../../../../pure3d/chunk-types/chunk-3F00001.md).

These chunks are static collision in the world made up of boxes, cylinders and spheres.

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `Zone.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

* `BaseZone`
	* Recommended.
* `Entities`
    * Not recommended.
* `Phys`
    * Not recommended.

# Syntax
```text
<StaticPhysName> [StaticPhys] [<ClassTypeID>] [<ATCEntry>] [<SoundResourceName>]
```

* **StaticPhysName**: The name of this Static Phys.
{{ snippet lucasmapbuilder/sketchup-models/group-tags/staticphys-parameters }}

# Group Structure
This tag should be applied to a group exclusively containing [CollisionBox](../../special-components.md#collisionbox), [CollisionCylinder](../../special-components.md#collisioncylinder) and/or [CollisionSphere](../../special-components.md#collisionsphere) components.

# Examples
TODO

# Other Tags
These are other tags that can be used with this to configure it further.

# Version History
## 1.0
Initial release.