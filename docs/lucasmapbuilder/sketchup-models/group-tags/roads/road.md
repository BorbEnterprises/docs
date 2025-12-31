---
title: Road
description: "This tag is used to create Roads. These are used by AI cars to navigate the world as well as the game's navigation system."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag is used to create [Roads](../../../../pure3d/chunk-types/chunk-3000003.md).

These are used by AI cars to navigate the world as well as the game's navigation system.

**Note**: Unless you need fine control over the shape of the segments, we recommend using the [SimpleRoad tag](simpleroad.md) instead.

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
<RoadName> [Road] [<StartIntersection>] [<EndIntersection>] [<MaxTraffic>] [<Lanes>]
```

* **RoadName**: The name of this road.
* **StartIntersection**: The name of the [Intersection](intersection.md) this road starts at.
* **EndIntersection**: The name of the [Intersection](intersection.md) this road ends at.
* **MaxTraffic**: The maximum amount of traffic cars that can be on this road at a time.
    * Use 0 to make a road that does not spawn traffic.
* **Lanes**: The amount of lanes this road will be divided into.

# Group Structure
This tag should be applied to a group containing other groups that each contain two lines drawn in opposing directions representing each segment of the road.

# Examples
TODO

# Other Tags
These are other tags that can be used with this to configure it further.

{{ snippet lucasmapbuilder/sketchup-models/group-tags/road-other-tags }}

# Version History
## 1.0
Initial release.