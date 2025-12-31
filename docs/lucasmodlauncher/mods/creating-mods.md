---
title: Creating Mods
description: "This page documents the basics of creating a mod."
---

Creating a mod is as simple as creating a folder inside any valid [Mod Directory](installing-mods.md#where-do-i-put-mods) with a file named `Meta.ini` inside it.

This file contains information about the mod such as the title, description(s), required hacks and authors. 

It should, at minimum, contain a `[Miscellaneous]` section with a `Title` property (which the end user will see) and an `InternalName` property (which is used internally by the Mod Launcher and the mod itself among other things).

Here's an example:

```ini
[Miscellaneous]
; The actual title of the mod displayed in the Mod's list.
Title=Example Mod

; The name used internally to refer to the Mod.
InternalName=ExampleMod
```

To actually do anything with this mod, you will need to require at least one hack. 

For example, a mod that just wants to override one file in the game folder would just require `CustomFiles` and create a folder named "CustomFiles".

```ini
RequiredHack=CustomFiles
```

For more detailed information about configuring the mod itself and the structure of a mod folder, see [Configuring Mods](configuring-mods.md).

For more detailed information about which hacks are requirable and which ones are also configurable see the list of [Mod Requirable hacks](../hacks/all-hacks#mod-requirable-hacks) and the individual pages for each hack.