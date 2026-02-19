---
title: "No Neither Road Arrow Processing"
description: "This hack fixes an issue where the game tries to process road arrows during a \"neither\" stage which can cause crashes in certain cases."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 387 # 1.21
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This hack fixes an issue where the game tries to process road arrows during a "neither" stage which can cause crashes in certain cases.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=NoNeitherRoadArrowProcessing
```