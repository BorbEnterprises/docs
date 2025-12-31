---
title: Waypoint
description: "This tag is used to create Type 0 Event Locators using Event 2. These are used as waypoints in missions."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 0 Event Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-8-directional-locator) using [Event 2](../../../../hitandrun/misc/events.md#event-2). 

These are used as waypoints in missions.

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
<LocatorName> [Waypoint]
```

* **LocatorName**: The name of the locator.

# Group Structure
This tag should be applied to a group containing a [Locator component](../../special-components.md#locator) and one or more [RectTriggerVolume](../../special-components.md#rect-trigger-volume) or [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) components.

# Examples
This is an example of a couple different groups with this tag applied to it:

![waypoint example](/img/lucasmapbuilder/sketchup-models/group-tags/locators/waypoint-example.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.