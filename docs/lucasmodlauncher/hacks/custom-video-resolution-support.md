---
title: Custom Video Resolution Support
description: "This hack increases the video segment size from 256x256 to a configurable amount."
---

**This hack can be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

**This hack is pseudo hack provided by [Increased Video Resolution Support](increased-video-resolution-support.md).**

This hack increases the video segment size from 256x256 to a configurable amount.

This allows mods to increase the maximum video resolution from about 768x768.
   
These limits do not apply to videos used as textures with [Video Texture Support](video-texture-support.md) as those are instead subject to texture-related limitations.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomVideoResolutionSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomVideoResolutionSupport.ini` and add the parameters necessary for your mod inside it.

```ini
[Miscellaneous]
SegmentWidth=2018
SegmentHeight=1024
```

# History
## 1.18
Added this pseudo hack. Don't poke at it.