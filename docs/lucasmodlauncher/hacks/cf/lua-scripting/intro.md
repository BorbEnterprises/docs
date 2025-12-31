---
title: Getting Started
description: "This hack utilises the Lua Support hack to allow mods to run Lua code to handle files when the game requests they be loaded. "
---

This hack utilises the [Lua Support](../../lua-support.md) hack to allow mods to run Lua code to handle files when the game requests they be loaded. 

Mods can define Lua code in two places:

* `CustomFiles.lua`: This is a script located in the root of the mod that will be executed as soon as the mod is loaded.
* Path Handlers: Mods can specify Lua scripts that will be executed when a specific file or files (via wildcards) are requested by the game using the hack's [configuration file](../intro.md#configuration).
    * These scripts are intended to go somewhere in a folder named "Resources" in the root of the mod.

This allows mods to do a number of powerful things such as redirect or manipulate the files being requested or generate new ones altogether.

# Allowed Functions/Variables
For a list of all of the stock Lua functions and variables that are allowed with this hack, see [Allowed Functions/Variables](allowed-functions-variables.md).

# Custom Functions
For a list of custom functions this hack provides, see [All Custom Lua Functions](custom-functions/all-functions.md).