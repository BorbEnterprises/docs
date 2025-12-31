---
title: Video Texture Support
description: "This hack allows you to use Bink video files as textures."
---

**This hack must be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

This hack allows you to use Bink video files as textures.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=VideoTextureSupport
```

# Using This Hack
Bink video files intended for use with this hack have the same restrictions that normal textures do. They must be powers of 2 on the width and height (32x32, 64x128, 256x512, etc.).

To add a video texture to your P3D file using [Lucas' Pure3D Editor](../../lucasp3deditor/intro.md), you just need to modify the "Texture" parameter of a [Shader](../../pure3d/chunk-types/chunk-11000.md). The value has to be a path starting with a `/` inside the Mod Launcher's file system.

It is recommended that you use `/GameData/` though other paths in the [Virtual File System](cf/virtual-file-system.md#mount-points) will also work.

![video texture example path](/img/lucasmodlauncher/hacks/video-texture-support/usage_p3deditor.png)

If the movie has transparency, it's also important to set the "Blend Mode" to "Alpha". Other Blend Modes are also supported.

# Debug Text Mode
This hack registers a [debug mode](debug-text.md#registered-by-video-texture-support) when used alongside [Debug Text](debug-text.md).

# History
## 1.19
Added this hack.