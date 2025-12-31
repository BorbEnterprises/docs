---
title: Intersection
description: "This tag is used to create Intersections. These are used to connect roads to each other to create a large interconnected network."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag is used to create [Intersections](../../../../pure3d/chunk-types/chunk-3000004.md).

These are used to connect roads to each other to create a large interconnected network.

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
<IntersectionName> [Intersection]
```

* **Intersection**: The name of this intersection to be referenced by the various road group tags.

# Group Structure
This tag should only be applied to a group containing a circle.

# Examples
TODO

# Other Tags
These are other tags that can be used with this to configure it further.

## Stop
This tag flags the intersection as being one that traffic should stop at momentarily when they reach it (a traffic behaviour index of 1).

```text
[Stop]
```

## TrafficBehaviour
This tag adds a custom traffic behaviour index to the intersection.

```text
[TrafficBehaviour] [<TrafficBehaviourIndex>]
```

* **TrafficBehaviourIndex**: The traffic behaviour index to use.
    * **1**: Traffic cars will stop when they reach the intersection.
    * **3**: Traffic cars will keep driving when they reach the intersection.
        * This is the default behaviour.

# Version History
## 1.0
Initial release.