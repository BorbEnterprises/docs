---
title: Event
description: "This tag is used to create Type 0 Event Locators with a customisable event and parameter."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 0 Event Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-8-directional-locator) with a customisable event and parameter.

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
<LocatorName> [Event] [<EventIndex>] [<EventParameter>]
```

* **LocatorName**: The name of the locator.
* **EventIndex**: The event index to trigger.
* **EventParameter**: The parameter to give to the event.

# Group Structure
This tag should be applied to a group containing a [Locator component](../../special-components.md#locator) and one or more [RectTriggerVolume](../../special-components.md#rect-trigger-volume) or [SphereTriggerVolume](../../special-components.md#sphere-trigger-volume) components.

# Examples
TODO

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.