---
title: StaticCam
description: "This tag is used to create Type 12 Static Cam Locators."
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag is used to create [Type 12 Static Cam Locators](../../../../pure3d/chunk-types/chunk-3000005.md#type-12-static-cam-locator).

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
<LocatorName> [StaticCam] [<FOV>]
```

* **LocatorName**: The name of the locator.
* **FOV**: The field of view for the camera.

# Group Structure
TODO

# Examples
TODO

# Other Tags
These are other tags that can be used with this to configure it further.

## FollowPlayer
This tag makes it so the camera targets an offset from the current position of the player.

```text
[FollowPlayer] [<X>] [<Y>] [<Z>]
```

* **X**: The X offset from the player's position.
* **Y**: The Y offset from the player's position.
* **Z**: The Z offset from the player's position.

**Note:** The players position is at their feet so you may want to at least have a Y offset.

## JumpCut
This tag makes it so the camera will immediately be in this position of the camera instead of panning over to it when entering the trigger.

```text
[JumpCut]
```

## InCarOnly
This tag makes it so the camera only works when the player is in a car.

```text
[InCarOnly]
```

## OnFootOnly
This tag makes it so the camera only works when the player is on foot.

```text
[OnFootOnly]
```

## TargetSpeed
TODO

```text
[TargetSpeed] [<Speed>]
```

* **Speed**: TODO.

## TransitionSpeed
TODO

```text
[TransitionSpeed] [<Speed>]
```

* **Speed**: TODO.

# Version History
## 1.0
Initial release.