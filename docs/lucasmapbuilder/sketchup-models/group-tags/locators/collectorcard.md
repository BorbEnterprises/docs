---
title: CollectorCard
description: "This tag is used to create Type 9 Action Event Locators with the CollectorCard type. These are used to spawn collector cards in the world."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 9 Action Event Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-9-action-event-locator) with the [CollectorCard type](../../../../hitandrun/misc/action-event-locator-types.md#collectorcard). 

These are used to spawn collector cards in the world.

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
<CardID> [CollectorCard]
```

* **CardID**: The ID of the collector card.
    * This is the word "card" followed by a level index and a card index.
    * For example, `card11` is Level 1's first collector card.

# Group Structure
This tag should be applied to a group containing a [Locator component](../../special-components.md#locator) and one or more [RectTriggerVolume](../../special-components.md#rect-trigger-volume) or [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) components.

Cards typically have a single [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) with a radius of 1 meter (which is the default scale of these components).

# Examples
This is an example of a group with this tag applied to it:

![collector card example](/img/lucasmapbuilder/sketchup-models/group-tags/locators/collectorcard-example.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.