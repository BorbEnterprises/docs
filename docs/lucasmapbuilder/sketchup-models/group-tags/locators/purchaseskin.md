---
title: PurchaseSkin
description: "This tag is used to create Type 9 Action Event Locators with the PurchaseSkin type. These are used to spawn skin shops in the world that the player can interact with to buy and switch to different outfits."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 9 Action Event Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-9-action-event-locator) with the [PurchaseSkin type](../../../../hitandrun/misc/action-event-locator-types.md#purchaseskin). 

These are used to spawn skin shops in the world that the player can interact with to buy and switch to different outfits.

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
<LocatorName> [PurchaseSkin]
```

* **LocatorName**: The name of the locator.

# Group Structure
This tag should be applied to a group containing a [Locator component](../../special-components.md#locator) and one or more [RectTriggerVolume](../../special-components.md#rect-trigger-volume) or [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) components.

Skin shops typically have a single [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) with a radius of about 1.25 meters.

# Examples
This is an example of a group with this tag applied to it:

![purchase skin example](/img/lucasmapbuilder/sketchup-models/group-tags/locators/purchaseskin-example.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.