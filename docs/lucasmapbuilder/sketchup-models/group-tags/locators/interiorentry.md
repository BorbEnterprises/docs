---
title: InteriorEntry
description: "This tag creates Type 7 Interior Entrance Locators. These are used to enter an interior."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 7 Interior Entrance Locators](../../../../pure3d/chunk-types/chunk-3000005.md#this_types_type7).

These are used to enter an interior.

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
<LocatorName> [InteriorEntry] [<InteriorName>]
```

* **LocatorName**: The name of the locator.
* **InteriorName**: The name of the interior this trigger will place the player inside.

# Group Structure
This tag should be applied to a group containing a [Locator component](../../special-components.md#locator) and one or more [RectTriggerVolume](../../special-components.md#rect-trigger-volume) or [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) components.

# Examples
This is an example of a group with this tag applied to it:

![interior entry group example](/img/lucasmapbuilder/sketchup-models/group-tags/locators/interiorentry-example.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.