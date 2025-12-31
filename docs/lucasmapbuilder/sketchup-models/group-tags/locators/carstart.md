---
title: CarStart
description: "This tag is used to create Type 3 Car Start Locators. These are used to position cars, characters and other miscellaneous things in missions."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 3 Car Start Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-3-car-start-locator).

These are used to position cars, characters and other miscellaneous things in missions.

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
<LocatorName> [CarStart]
```

* **LocatorName**: The name of the car start locator.

# Group Structure
This tag should only be applied directly to a [Locator component](../../special-components.md#locator).

# Examples
TODO

# Other Tags
These are other tags that can be used with this tag to configure it further.

## ParkedCar
This tag flags the locator as being a parked car spawn point.

```text
LocatorName [CarStart] [ParkedCar]
```

## FreeCar
This tag flags the locator as being a spawn point for a free car (the level's bonus car).

```text
LocatorName [CarStart] [FreeCar] [<CarName>]
```

* **CarName**: The name of the free car to spawn.

# Version History
## 1.0
Initial release.