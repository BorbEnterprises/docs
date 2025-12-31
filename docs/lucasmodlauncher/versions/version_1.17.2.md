---
title: Version 1.17.2
description: "This update was released on May 11th, 2018."
authors: ["loren","lucasc190"]
---

**This update was released on May 11th, 2018.**

# Hacks
## Custom Character Support
Added the `BlendModeSupport` property to characters that allows the usage of Additive and Subtractive shaders.

Here's a version of Homer with his shader set to Additive:

![additive homer](/img/lucasmodlauncher/misc/additive_homer.png)

```ini
[h_glow]
BlendModeSupport=1
```

## Custom Limits
Added support for a `[Billboards]` section that can define a `QuadGroupLimit` and a `QuadLimit`.

## Debug Checks
Changed the name of the Missing Locator Detection setting to Experimental Missing Locator Detection.

## Debug Test

* Added "No Cursor Until Mouse Move" in the Menus tab.
* Added "No Suppressed Drivers" in the Miscellaneous tab.

## Increased Reward Limit
Increased the limit of car attributes registered with SetCarAttributes from 50 to infinity.

## Modern Computer Support
Made the game support running from the `A:` and `B:` drives.