---
title: DeathZone
description: "This tag is used to create Type 0 Event Locators using Event 4. These are used to reset the player when they enter its triggers."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 0 Event Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-8-directional-locator) using [Event 4](../../../../hitandrun/misc/events.md#event-4). 

These are used to reset the player when they enter its triggers.

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
<LocatorName> [DeathZone]
```

* **LocatorName**: The name of the locator.

# Group Structure
This tag should be applied to a group containing a [Locator component](../../special-components.md#locator) and one or more [RectTriggerVolume](../../special-components.md#rect-trigger-volume) or [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) components.

Alternatively, the group can contain *two* [Locator components](../../special-components.md#locator) with one named "Car" and the other named "Player" to set separate respawn points for cars and characters.

# Examples
This is an example of a couple different groups with this tag applied to it:

![death zone example](/img/lucasmapbuilder/sketchup-models/group-tags/locators/deathzone-example.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.