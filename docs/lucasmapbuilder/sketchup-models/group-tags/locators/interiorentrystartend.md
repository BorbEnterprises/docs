---
title: InteriorEntryStartEnd
description: "This tag is used to create Type 8 Directional Locators. These are used to position the player when they enter an interior."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 8 Directional Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-8-directional-locator).

These are used to position the player when they enter an interior.

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
<LocatorName> [InteriorEntryStartEnd]
```

* **LocatorName**: The name of the locator. 
    * Due to how the game uses this type of locator, this should only ever be `InteriorEntryStart` or `InteriorEntryEnd`.

# Group Structure
This tag should only be applied directly to a [Locator component](../../special-components.md#locator).

# Examples
TODO

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.