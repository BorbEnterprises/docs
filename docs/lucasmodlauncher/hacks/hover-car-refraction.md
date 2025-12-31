---
title: Hover Car Refraction
description: "This hack reimplements the refraction effect for Professor Frink's Hover Car from the console versions of the game."
---

**This hack can be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List.**

This hack reimplements the refraction effect for Professor Frink's Hover Car from the console versions of the game. This reimplementation is based on the Xbox version.

# Settings
## Per Car Screen Capture
This setting makes it so the game will capture the screen before rendering each hover car instead of just when the first one renders. This improves the appearance of multiple hover cars.

**Defaults to Enabled.**

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=HoverCarRefraction
```

When required, this hack will make all the necessary changes to the shaders of `art\\cars\\frink_v.p3d` **unless** the mod requiring it provides it, in which case the mod will be expected to make the changes to the shader on its own.

<!-- TODO: document this in greater detail -->

# Version History
## 1.26
{{ snippet lucasmodlauncher/versions/1.26/hack_hover-car-refraction }}

## 1.23.5
Added a description to this hack.

## 1.23.4
Added this hack.