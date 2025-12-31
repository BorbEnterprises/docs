---
title: game.lua Script
description: "This resource is a Lua script that makes it easy to script levels and missions in Custom Files Lua Path Handler scripts."
---

This resource is a Lua script that makes it easy to script levels and missions in Custom Files Lua Path Handler scripts by obscuring the calls to the [Output](../../../../lucasmodlauncher/hacks/cf/lua-scripting/custom-functions/output.md) Lua function available in [Custom Files](../../../../lucasmodlauncher/hacks/cf/intro.md) Lua path handler scripts.

# Download
This script is available from the [Donut Team downloads page](https://donutteam.com/downloads/GameLua).

# Usage
Simply place the script somewhere in your mod's "Resources" folder and load it in `CustomFiles.lua`:

```lua
dofile(GetModPath() .. "/Resources/scripts/game.lua")
```

Then you can add a `[PathHandlers]` entry for any MFK script and write scripts in more or less the same way with some notable differences:

* All commands must be prefixed with `Game.` since the script stores them in a table called `Game`.
	* This is done for organizational reasons as flooding the global table with 250-300 functions would be messy.
* You don't need to have `;` after function calls because Lua doesn't require them (though it doesn't hurt to have them).
* Unlike MFK, strings must *always* be in quotes.
    * This is notable because Radical omits quotes in a few places as their basic scripting didn't require it.
* Backslashes `\` must be escaped with another backslash like `\\`.
* Writing conditional command blocks works differently. See the [Conditionals](#technical-details_conditionals) section below for more details.

Here's some example comparisons of one of Radical's function calls and how it would look in Lua:

{{ tabs }}
{{ tab MFK }}
```text
LoadP3DFile("art\missions\level01\m0.p3d");
```
```js
// Radical often didn't use quotes on their locator names for this command.
GagSetTrigger("action", JasperTrig, 2);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.LoadP3DFile("art\\missions\\level01\\m0.p3d")
```
```lua
-- So you would need to add them for Lua.
Game.GagSetTrigger("action", "JasperTrig", 2)
```
{{ endtab }}
{{ endtabs }}

Now here's an example path handler:

```ini
[PathHandlers]
scripts\\missions\\level01\\m0.mfk=Resources/scripts/missions/level01/m0.lua
```

And the contents of the script for it:

```lua
Game.SelectMission("m0")
	Game.SetMissionResetPlayerInCar("level1_carstart")
	Game.SetDynaLoadData("l1z1.p3d;l1r1.p3d;l1r7.p3d;")

	Game.UsePedGroup(0) 

	Game.AddStage(1)
        Game.RESET_TO_HERE()
        
		Game.SetHUDIcon("kwike")
		Game.SetStageMessageIndex(131)
		
		Game.AddObjective("dummy")
		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```

# Technical Details
The script has a local function called `OutputCommand` and a table named `Game` containing functions for each script command in the base game that use it.

The functions call `OutputCommand` with the given function name and any arguments given to it. This function then assembles a string of the command call and then calls [Output](/lucasmodlauncher/hacks/cf/lua-scripting/custom-functions/output.md) to write it to the virtual script.

If the [Additional Script Functionality](/lucasmodlauncher/hacks/asf/intro.md) hack is loaded, additional functions are registered for the commands it adds.

## Conditionals
ASF adds conditional commands such as [IfCurrentCheckpoint](/lucasmodlauncher/hacks/asf/mfk-commands/ifcurrentcheckpoint.md).

These commands are expected to be followed by a conditional block opened with `{` and closed with a `}`.

Since there is no way to represent this in that manner with Lua, `OutputCommand` handles outputting the opening `{` and you must close it with `Game.EndIf()` (which just outputs `}`).

Here are some examples of the same conditional block written in MFK and in a path handler using this script:

{{ tabs }}   
{{ tab MFK }}
```js
IfCurrentCheckpoint()
{
	SetStageTime(20);
}
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.IfCurrentCheckpoint()
	SetStageTime(20)
Game.EndIf()
```
{{ endtab }}
{{ endtabs }}

# Credits
This script was created by Donut Team.

# Version History
## Version 3

* Changed it so instead of iterating arrays each time its loaded, the script just registers a bunch of functions directly.
* Added new commands Version 1.25 of the Mod Launcher.
	* Also updated `OutputCommand` to support conditionals and adding the new `Game.EndIf` function.

## September 14th, 2019
Updated the ASF table with the `SetCollectibleSoundEffect` command added in Version 1.23.5 of the Mod Launcher.

## July 28th, 2019
Initial release.