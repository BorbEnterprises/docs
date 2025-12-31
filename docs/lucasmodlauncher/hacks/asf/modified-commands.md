---
title: Modified Commands
description: "This page documents script commands from the base game that are modified by this hack to have expanded functionality."
---

This page documents script commands from the base game that are modified by this hack to have expanded functionality.

## SetDurationTime

**Modified as of Version 1.18.**

Modified to support milliseconds.

{{ tabs }}
{{ tab MFK }}
```js
SetDurationTime(1.5);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetDurationTime(1.5)
```
{{ endtab }}
{{ endtabs }}

Learn more about the original command [here](/hitandrun/scripting/mfk-commands/setdurationtime.md).

## SetHitAndRunDecayInterior

**Modified as of Version 1.18.**

Modified to work. By default, this command is broken since it is mapped to the wrong function in the game's code.

{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunDecayInterior(4.0);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunDecayInterior(4.0)
```
{{ endtab }}
{{ endtabs }}

Learn more about the original command [here](/hitandrun/scripting/mfk-commands/sethitandrundecayinterior.md).