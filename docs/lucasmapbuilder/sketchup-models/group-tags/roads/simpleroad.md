---
title: SimpleRoad
description: "This tag is used to create Roads. These are used by AI cars to navigate the world as well as the game's navigation system."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag is used to create [Roads](../../../../pure3d/chunk-types/chunk-3000003.md).

These are used by AI cars to navigate the world as well as the game's navigation system.

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
<RoadName> [SimpleRoad] [<StartIntersection>] [<EndIntersection>] [<MaxTraffic>] [<Lanes>] [<Width>]
```

* **RoadName**: The name of this road.
* **StartIntersection**: The name of the [Intersection](intersection.md) this road starts at.
* **EndIntersection**: The name of the [Intersection](intersection.md) this road ends at.
* **MaxTraffic**: The maximum amount of traffic cars that can be on this road at a time.
    * Use 0 to make a road that does not spawn traffic.
* **Lanes**: The amount of lanes this road will be divided into.
* **Width**: The width of the road in meters.

# Group Structure
This tag should be applied to a group containing a single interconnected line from the start intersection to the end intersection.

# Examples
TODO

# Other Tags
These are other tags that can be used with this to configure it further.

{{ snippet lucasmapbuilder/sketchup-models/group-tags/road-other-tags }}

# Version History
## 1.0
Initial release.