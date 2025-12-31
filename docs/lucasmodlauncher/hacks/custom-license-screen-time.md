---
title: Custom License Screen Time
description: "This hack allows mods to adjust the amount of time spent on the license screen and whether or not the user is able to prematurely skip it."
---

**This hack must be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

This hack allows mods to adjust the amount of time spent on the license screen and whether or not the user is able to prematurely skip it.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomLicenseScreenTime
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomLicenseScreenTime.ini` and add the parameters necessary for your mod inside it.

```ini
; [Miscellaneous] Section
	; Time: In Milliseconds. 
		; Defaults to 1000
	; Skippable: Set if the license screen can be skipped with Enter. 
		; Defaults to 0.

; Notes
	; Setting Time to -1 and Skippable to 0 makes it impossible to bypass the license screen.

[Miscellaneous]
Time=1000
Skippable=0
```

# Version History
## 1.5
Added this hack.