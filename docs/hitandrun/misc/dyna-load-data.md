---
title: Dyna Load Data Strings
description: "This page documents Dyna Load Data Strings used in Type 5 Zone Event Locators and various script commands."
---

This page documents Dyna Load Data Strings used in [Type 5 Zone Event Locators](../../pure3d/chunk-types/chunk-3000005.md#type-5-zone-event-locator) and various script commands such as [SetDynaLoadData](../scripting/mfk-commands/setdynaloaddata.md).

These strings define instructions to load and unload zones of the world (file names relative to the "art" folder). 

They can also enable and disable [World Spheres](../../pure3d/chunk-types/chunk-3F0000B.md).

# Symbols
This table contains the various symbols used in these strings and what type of purpose they serve.

| Symbol | Purpose              |
|--------|----------------------|
| ;      | Region Load          |
| :      | Region Unload        |
| @      | Interior Load        |
| $      | Interior Unload      |
| *      | Enable World Sphere  |
| &      | Disable World Sphere |

# Examples
Dyna Load Data is a series of file names (relative to the art folder) or World Sphere names followed by the aforementioned symbols to load/unload or enable/disable them.

Here are some examples:

```text
l1z3.p3d:l1z4.p3d:l1z6.p3d:l1z7.p3d:l1r3.p3d:l1r4a.p3d:l1r4b.p3d:l1r6.p3d:l1r7.p3d:l1z1.p3d;l1r1.p3d;l1z2.p3d;l1r2.p3d;
```
```text
visibility_testController&
```
```text
l1z7.p3d:l1z2.p3d:l1i02.p3d@
```