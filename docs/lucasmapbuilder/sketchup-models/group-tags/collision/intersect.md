---
title: Intersect
description: "This tag is used to create Intersect collision out of the contents of the group it is applied to. This type of collision is essentially used as the ground of a level."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Intersect collision](../../../../pure3d/chunk-types/chunk-3F00003.md) out of the contents of the group it is applied to.

This type of collision is essentially used as the ground of a level.

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `Zone.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

* `BaseZone`
	* Recommended.
* `Entities`
	* Not recommended.
* `Intersects`
	* Not recommended.

# Syntax
```text
GroupName [Intersect]
```

# Group Structure
This tag can be used on any group containing geometry.

# Examples
These are examples of groups with these tags applied to them.

![intersect example](/img/lucasmapbuilder/sketchup-models/group-tags/collision/intersect-example1.png)

# Other Tags
These are other tags that can be used with this tag to configure it further.

These can either be used alongside the `[Intersect]` tag or on groups inside a group that have that tag applied to them.

## Grass
This tag makes the intersects have a grass surface type index (1).

```text
GroupName [Intersect] [Grass]
```

## Sand
This tag makes the intersects have a sand surface type index (2).

```text
GroupName [Intersect] [Sand]
```

## Water
This tag makes the intersects have a water surface type index (4).

```text
GroupName [Intersect] [Water]
```

## Dirt
This tag makes the intersects have a dirt surface type index (7).

```text
GroupName [Intersect] [Dirt]
```

## SurfaceType
This tag makes the intersects have the specified surface type index.

```text
GroupName [Intersect] [SurfaceType] [<SurfaceTypeIndex>]
```

* **SurfaceTypeIndex**: The surface type index you'd like to use.

# Version History
## 1.0
Initial release.