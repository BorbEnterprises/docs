---
title: Coin
description: "This tag is used to create Type 14 Locators. These locators spawn a single coin at their position."
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 14 Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-3-car-start-locator).

These locators spawn a single coin at their position.

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
<LocatorName> [Coin]
```

* **LocatorName**: The name of the locator.

# Group Structure
This tag should only be applied directly to a [Locator component](../../special-components.md#locator).

# Examples
This is an example of a group with this tag applied to it:

![coin example](/img/lucasmapbuilder/sketchup-models/group-tags/locators/coin-example.png)

# Other Tags
There are no other other tags that can be used with this tag to configure it further.

# Version History
## 1.0
Initial release.