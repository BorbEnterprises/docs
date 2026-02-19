---
title: "No Busted Hit & Run Meter Reset"
description: "This makes it so the Hit & Run meter will not reset and the music will not end when you get busted by the police."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 399 # 1.23.6
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/MustBeRequiredByMod.md }}

This makes it so the Hit & Run meter will not reset and the music will not end when you get busted by the police.

This hack expects the mod to actually set the decay to 0 alongside requiring it.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=NoBustedHitAndRunMeterReset
```