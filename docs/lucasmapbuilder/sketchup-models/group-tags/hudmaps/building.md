---
title: Building
description: "This tag makes a group's geometry get included in the HUD Map Mesh with the same color Radical used to represent buildings (a white-ish color)."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag makes a group's geometry get included in the HUD Map [Mesh](../../../xml-format/elements/entities/mesh.md) with the same color Radical used to represent buildings (a white-ish color).

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `HUDMap.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

* `BaseHUDMap`

# Syntax
```
GroupName [Building]
```

# Group Structure
This tag can be applied to a group containing anything though its optimal to use a simplified group with no overlapping geometry that represents what you want when possible as the meshes will get flattened in the process of becoming the HUD map.

# Examples
TODO

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.