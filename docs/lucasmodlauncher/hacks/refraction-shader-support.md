---
title: Refraction Shader Support
description: "This hack reimplements the refract PDDI shader."
---

**This hack must be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

This hack reimplements the `refract` PDDI shader.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=RefractionShaderSupport
```

# Known Issues
While this hack is currently able to be required by mods, there are some issues with doing so when using the shader on multiple entities (like multiple cars or characters). This is due to the game only capturing the screen once the first time something with a `refract` shader is rendered on the frame.

The [Hover Car Refraction](hover-car-refraction.md) hack uses this hack but has its own explicit support for multiple *Hover Cars* existing but nothing more.

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-refraction-shader-support) for the Mod Launcher.

# Version History
## 1.26
{{ snippet lucasmodlauncher/versions/1.26/hack_refraction-shader-support }}

## 1.23.4
Added this hack.