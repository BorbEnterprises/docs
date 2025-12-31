---
title: PedGroup
description: "This tag is used to create Type 13 Ped Group Locators. These locators change the active ped group when you enter their triggers."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 13 Ped Group Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-13-ped-group-locators).

These locators change the active ped group when you enter their triggers.

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `Zone.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

* `BaseZone`
	* Recommended when building an entire zone.
* `Locators2`
	* Recommended when building a group that only contains locators.
* `Entities`
	* Not recommended.

# Syntax
```text
<LocatorName> [PedGroup] [<PedGroupIndex>]
```

* **LocatorName**: The name of the locator.
* **PedGroupIndex**: The ped group index to switch to.

# Group Structure
This tag can be applied to directly to [RectTriggerVolume](../../special-components.md#rect-trigger-volume) or [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) components or to a group containing one or more of them.

# Examples
This is an example of a trigger component and a group with this tag applied to it:

![ped group example](/img/lucasmapbuilder/sketchup-models/group-tags/locators/pedgroup-example.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.