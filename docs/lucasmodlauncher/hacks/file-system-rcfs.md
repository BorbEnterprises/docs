---
title: File System RCFs
description: "This hack makes the game's RCF files get mounted into the virtual file system, allowing their contents to be accessed by Lua scripts."
---

**This hack can be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List (hidden by default).**

This hack makes the game's RCF files get mounted into the virtual file system, allowing their contents to be accessed by Lua scripts.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=FileSystemRCFs
```

# Version History
## 1.25
{{ snippet lucasmodlauncher/versions/1.25/hack_file-system-rcfs }}

## 1.24
Added this hack.