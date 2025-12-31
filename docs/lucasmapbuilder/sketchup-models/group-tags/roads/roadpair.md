---
title: RoadPairLeft / RoadPairRight
description: "These tags are used to create pairs of Roads. These are used by AI cars to navigate the world as well as the game's navigation system."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

These tags are used to create pairs of [Roads](../../../../pure3d/chunk-types/chunk-3000003.md) going in opposite directions.

These are used by AI cars to navigate the world as well as the game's navigation system.

**Note**: Unless you need fine control over the shape of the road segments, we recommend using the [SimpleRoadPair tags](simpleroadpair.md) instead.

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
<RoadPairName> [RoadPairLeft] [<MaxTraffic>] [<Lanes>]
```
```text
<RoadPairName> [RoadPairRight] [<MaxTraffic>] [<Lanes>]
```

* **RoadPairName**: The name of these roads. One side will have its name adjusted to be unique.
* **MaxTraffic**: The maximum amount of traffic cars that can be on this road at a time.
    * Use 0 to make a road that does not spawn traffic.
* **Lanes**: The amount of lanes this road will be divided into.

The width of the road is half the width of the pair.

The start and end intersections are determined automatically though they can also be explicitly controlled with the [`Intersections`](#intersections) tag below.

The two different tags determine which side of the road the cars drive on.

# Group Structure
This tag should be applied to a group containing other groups that each contain two lines drawn in opposing directions representing each segment of both sides of the road pair. These segments should start and end at two different [Intersections](intersection.md).

# Examples
TODO

# Other Tags
These are other tags that can be used with this to configure it further.

## Intersections
This tag will allow you to manually control the start and end intersections for the road pair.

```text
[Intersections] [<Intersection1>] [<Intersection2>]
```

* **Intersection1**: The first intersection for the road pair.
* **Intersection2**: The second intersection for the road pair.

{{ snippet lucasmapbuilder/sketchup-models/group-tags/road-other-tags }}

# Version History
## 1.0
Initial release.