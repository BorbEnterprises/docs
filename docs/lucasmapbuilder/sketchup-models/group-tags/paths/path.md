---
title: Path / PathReversed
description: "These tags create Paths. These are used to spawn pedestrians and allows them to walk around."
summary:
    initialVersion: "1.0"
---

These tags create [Paths](../../../../pure3d/chunk-types/chunk-300000B.md).

These are used to spawn pedestrians and allows them to walk around.

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `Zone.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

* `BaseZone`
	* Recommended.
* `Entities`
	* Not recommended.
* `Paths`
	* Not recommended.

# Syntax
```text
GroupName [Path]
```
```text
GroupName [PathReversed]
```

These two tags build the same chunk type, the latter just reverses the order of the points.

# Group Structure
These tags should be applied to a group containing a series of interconnected lines wherein the lines form a complete shape. There should be no more than 32 points in this line.

# Examples
This is an example of the simple group structure required for this tag:

![path group structure](/img/lucasmapbuilder/sketchup-models/group-tags/paths/path-example-1.png)

This is an example of the actual contents of that group:

![path group contents](/img/lucasmapbuilder/sketchup-models/group-tags/paths/path-example-2.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.