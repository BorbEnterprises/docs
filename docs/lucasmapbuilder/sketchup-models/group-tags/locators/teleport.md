---
title: Teleport
description: "This tag is used to create Type 9 Action Event Locators with the Teleport type. These allow the player to interact with the locator's trigger(s) to be teleported to the location of the locator itself."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 9 Action Event Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-9-action-event-locator) with the [Teleport type](../../../../hitandrun/misc/action-event-locator-types.md#teleport). 

These allow the player to interact with the locator's trigger(s) to be teleported to the location of the locator itself.

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
<LocatorName> [Teleport]
```

* **LocatorName**: The name of the car start locator.

# Group Structure
This tag should be applied to a group containing a [Locator component](../../special-components.md#locator) and one or more [RectTriggerVolume](../../special-components.md#rect-trigger-volume) or [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) components.

# Examples
This is an example of a group with this tag applied to it:

![teleporter example](/img/lucasmapbuilder/sketchup-models/group-tags/locators/teleporter-example.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.