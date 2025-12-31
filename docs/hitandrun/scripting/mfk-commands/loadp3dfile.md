---
title: LoadP3DFile
description: "Loads a P3D file."
authors: ["loren"]
---

This command loads a P3D file.

# Context
{{ snippet hitandrun/command-contexts/any-load }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
LoadP3DFile( filepath, allocator, slot );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.LoadP3DFile( filepath, allocator, slot )
```
{{ endtab }}
{{ endtabs }}

* **filepath**: The path to the P3D file to load.
    * The following 6 paths are ignored since the game loads them at startup:
        * `art\phonecamera.p3d`
        * `art\cards.p3d`
        * `art\wrench.p3d`
        * `art\missions\generic\missgen.p3d`
        * `art\cars\common.p3d`
        * `art\cars\huskA.p3d`
* **allocator**: Set the memory allocator to use for this P3D file.
    * **GMA_DEFAULT**: Unknown.
    * **GMA_TEMP**: Unknown.
    * **GMA_PERSISTENT**: Unknown.
    * **GMA_LEVEL**: Unknown.
    * **GMA_LEVEL_MOVIE**: Unknown.
    * **GMA_LEVEL_FE**: Unknown.
    * **GMA_LEVEL_ZONE**: Unknown.
    * **GMA_LEVEL_OTHER**: Unknown.
        * Typically used for a level's FX file, for example `art\l01_fx.p3d`.
    * **GMA_LEVEL_HUD**: Unknown.
    * **GMA_LEVEL_MISSION**: Unknown.
    * **GMA_LEVEL_AUDIO**: Unknown.
    * **GMA_DEBUG**: Unknown.
    * **GMA_SPECIAL**: Unknown.
* **slot**: Unknown.
    * **Global**: Unknown.

# Examples
{{ tabs }}
{{ tab MFK }}
```text
// Load the level's locators.
LoadP3DFile("art\missions\level01\level.p3d");

// Load the Level's FX file into GMA_LEVEL_OTHER
LoadP3DFile("art\l01_fx.p3d","GMA_LEVEL_OTHER");

// Will be ignored.
LoadP3DFile("art\cars\huskA.p3d");
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Load the level's locators.
Game.LoadP3DFile("art\\missions\\level01\\level.p3d")

-- Load the Level's FX file into GMA_LEVEL_OTHER
Game.LoadP3DFile("art\\l01_fx.p3d","GMA_LEVEL_OTHER")

-- Will be ignored.
Game.LoadP3DFile("art\\cars\\huskA.p3d")
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.