---
title: Increased Video Resolution Support
description: "This hack increases the video segment size from 256x256 to 2048x1024."
---

**This hack must be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

This hack increases the video segment size from 256x256 to 2048x1024.

This increases the maximum video resolution from about 768x768 to about 6144x3072.
   
These limits do not apply to videos used as textures with [Video Texture Support](video-texture-support.md) as those are instead subject to texture-related limitations.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=IncreasedVideoResolutionSupport
```

# Version History
## 1.18
This hack now removes memory restrictions when playing RMV files.

## 1.15.3

* Changed the video segment size from 1024x512 to 2048x1024 to allow higher resolution videos (up to about 6144x3072 instead of 3072x1536).
* Fixed an issue causing videos to display incorrectly in the non-English versions of the game.

## 1.11
Added this hack.