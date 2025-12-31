---
title: SummonVehiclePhone
description: "This tag is used to create Type 9 Action Event Locators with the SummonVehiclePhone type. These allow the player to open the phonebooth menu to spawn a car."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 9 Action Event Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-9-action-event-locator) with the [SummonVehiclePhone type](../../../../hitandrun/misc/action-event-locator-types.md#summonvehiclephone). 

These allow the player to open the phonebooth menu to spawn a car.

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
<LocatorName> [SummonVehiclePhone]
```

* **LocatorName**: The name of the locator.
    * Note that these locators also require a [CarStart](carstart.md) locator of the same name to exist as this is where they spawn the car.

# Group Structure
This tag should be applied to a group containing two [Locator components](../../special-components.md#locator) and one or more [RectTriggerVolume](../../special-components.md#rect-trigger-volume) or [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) components.

One of the two [Locator components](../../special-components.md#locator) should be named "Camera", this one will represent the base position of the camera used when summoning a car.

The other [Locator component](../../special-components.md#locator) represents the position of the floating phone icon.

Typically, Radical uses a [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) for phonebooths.

# Examples
This is an example of a group with this tag applied to it:

![summon vehicle phone group example](/img/lucasmapbuilder/sketchup-models/group-tags/locators/summonvehiclephone-example-1.png)

This is an example of the contents of that group in SketchUp's 3D view:

![summon vehicle phone group contents](/img/lucasmapbuilder/sketchup-models/group-tags/locators/summonvehiclephone-example-2.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.