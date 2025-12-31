---
title: HUDMap
description: "This tag changes the OutputHUDMapMesh parameter of the group it is applied to."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag changes the OutputHUDMapMesh parameter of the group it is applied to.

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `HUDMap.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

* `BaseHUDMap`

# Syntax
```
GroupName [HUDMap] [<MeshName>]
```

* **MeshName**: The name of the [Mesh](../../../xml-format/elements/entities/mesh.md) to use for this HUD map.

# Group Structure
This tag can be applied to any group.

The contents of the group will **NOT** inherently become part of the hud map, you must still use another hud map tag such as [`Building`](building.md), [`Road`](road.md) or [`Sidewalk`](sidewalk.md).

# Examples
TODO

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.