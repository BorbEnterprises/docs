---
title: LoadZone
description: "This tag is used to create Type 5 Zone Event Locators. These locators trigger the loading and unloading of map zones and interiors when the player drives into their triggers."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 5 Zone Event Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-5-zone-event-locator).

These locators trigger the loading and unloading of map zones and interiors when the player drives into their triggers.

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
<LocatorName> [LoadZone] [<DynaLoadString>]
```

* **LocatorName**: The name of the locator.
* **DynaLoadString**: The [Dyna Load Data String](../../../../hitandrun/misc/dyna-load-data.md) to execute when the player enters this load zone.

# Group Structure
This tag should be applied to a group containing a [Locator component](../../special-components.md#locator) and one or more [RectTriggerVolume](../../special-components.md#rect-trigger-volume) or [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) components.

# Examples
This is an example of a group with this tag applied to it:

![load zone group structure](/img/lucasmapbuilder/sketchup-models/group-tags/locators/loadzone-example.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.