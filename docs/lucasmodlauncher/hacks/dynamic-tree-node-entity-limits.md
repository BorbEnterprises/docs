---
title: Dynamic Tree Node Entity Limits
description: "This hack makes it so tree node entity limits get increased when their lists become full instead of corrupting the game."
---

**This hack can be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

**This is a [setting hack](all-hacks.md#setting-hacks) that can be enabled on the "Settings" page of the Mods List (hidden by default).**

This hack makes it so [tree node](../../pure3d/chunk-types/chunk-3F00004.md#tree-node-child-tree-node-2-0x3f00006) entity limits get increased when their lists become full instead of corrupting the game.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=DynamicTreeNodeEntityLimits
```

# Version History
## 1.23
Added a description to this hack.

## 1.22
Added this hack.