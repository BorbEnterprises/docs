---
title: FenceCW / FenceCCW
description: "This tag is used to create Fences. These are infinitely high vertical collision that's typically used to keep the player within the bounds of the map."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Fences](../../../../pure3d/chunk-types/chunk-3F00007.md).

These are infinitely high vertical collision that's typically used to keep the player within the bounds of the map.

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `Zone.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

* `BaseZone`
	* Recommended.
* `Entities`
	* Not recommended.

# Syntax
```text
GroupName [FenceCW]
```
```text
GroupName [FenceCCW]
```

The two different tags determine the direction the fences are facing.

# Group Structure
This tag should be applied to a group that only contains lines.

# Examples
This is an example of a group with this tag applied to it:

![fence example](/img/lucasmapbuilder/sketchup-models/group-tags/collision/fence-example.png)

Furthermore, the example video below shows lines being drawn counter clockwise to form a complete shape. Afterwards, the face that was created is deleted.

A group containing the lines as drawn would have collision facing outwards with the `[Fence]` tag and inwards with the `[FenceCCW]` tag.

[Example Video](https://cdn.donutteam.com/AdministratorUploads/DTDocs/LucasModelBuilder/SketchUpModels/GroupTags/Collision/FenceExample.mp4)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.