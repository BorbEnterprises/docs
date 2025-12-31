---
title: NoCollision
description: "This tag nullifies any other collision tags and components inside the group its applied to."
summary:
    initialVersion: "1.0"
---

This tag nullifies any other collision tags and components inside the group its applied to.

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `Drawables.xml`
* `StateProp.xml`
* `Vehicle.xml`
* `Zone.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

* `BaseZone`
	* Recommended.
    * Only when including `Zone.xml`.
* `StateProp`
	* Recommended.
    * Only when including `StateProp.xml`.
* `Vehicle`
	* Recommended.
    * Only when including `Vehicle.xml`.
* `Anim`
	* Not recommended.
    * Only when including `Drawables.xml`.
* `ArticulatedAnim`
	* Not recommended.
    * Only when including `Drawables.xml`.
* `Mesh`
	* Not recommended.
    * Only when including `Drawables.xml`.
* `Scenegraph`
	* Not recommended.
    * Only when including `Drawables.xml`.
* `ZoneVehicleOrStateProp`
	* Not recommended.
    * Only when including `Drawables.xml`, `StateProp.xml`, `Vehicle.xml` or `Zone.xml`.

# Syntax
```text
GroupName [NoCollision]
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