---
title: Spring
description: "This tag is used to create Type 0 Event Locators using Event 6. These are used to make \"springs\" that bounce the player towards the position of the locator."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 0 Event Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-8-directional-locator) using [Event 6](../../../../hitandrun/misc/events.md#event-6). 

These are used to make "springs" that bounce the player towards the position of the locator.

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
<LocatorName> [Spring]
```

* **LocatorName**: The name of the locator.

# Group Structure
This tag should be applied to a group containing a [Locator component](../../special-components.md#locator) and one or more [RectTriggerVolume](../../special-components.md#rect-trigger-volume) or [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) components.

The position of the locator component is where the player will get bounced towards.

# Examples
This is an example of a group with this tag applied to it:

![spring group structure](/img/lucasmapbuilder/sketchup-models/group-tags/locators/spring-example-1.png)

This is an example of the contents of that group in SketchUp's 3D view:

![spring group contents](/img/lucasmapbuilder/sketchup-models/group-tags/locators/spring-example-2.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.