---
title: "Anti-aliasing"
description: "This hack adds support for multisample anti-aliasing to the game."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 393 # 1.23
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack adds support for multisample anti-aliasing to the game. 

The level of anti-aliasing can be selected in the hack's settings in the Mod Info panel.

This hack will not be listed in the Mods List if your graphics card does not support anti-aliasing.

# Settings
## Anti-aliasing
The level of anti-aliasing to use.

**Defaults to the highest supported by your graphics card.**

# Command Line Arguments
This hack is affected by certain [[../CommandLineArguments.md]] for the Mod Launcher.