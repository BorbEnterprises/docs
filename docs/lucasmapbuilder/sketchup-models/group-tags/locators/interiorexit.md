---
title: InteriorExit
description: "This tag is used to create Type 0 Event Locators using Event 5. These are used to exit interiors."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 0 Event Locators](../../../../pure3d/chunk-types/chunk-3000005.md#this_types_type0) using [Event 5](/hitandrun/misc/events.md#event-5).

These are used to exit interiors.

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
<LocatorName> [InteriorExit]
```

* **LocatorName**: The name of the locator.

# Examples
This is an example of a group with this tag applied to it:

![interior exit group example](/img/lucasmapbuilder/sketchup-models/group-tags/locators/interiorexit-example.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.