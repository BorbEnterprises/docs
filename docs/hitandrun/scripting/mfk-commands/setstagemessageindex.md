---
title: SetStageMessageIndex
description: "Sets the stage objective text message index to use."
---

This command sets the stage objective text message index to use.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageMessageIndex( index );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageMessageIndex( index )
```
{{ endtab }}
{{ endtabs }}

* **index**: The index to use. Valid values are from 0-299.
    * This uses the text strings that begin with `MISSION_OBJECTIVE_` out of the text bible and [Custom Text](/lucasmodlauncher/hacks/custom-text.md#configuration) configuration files.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
    SetStageMessageIndex(174);

    AddObjective("dummy");
    CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
    Game.SetStageMessageIndex(174)

    Game.AddObjective("dummy")
    Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
When used in locked stages, this command uses the text strings that begin with `INGAME_MESSAGE_` out of the text bible and [Custom Text](/lucasmodlauncher/hacks/custom-text.md#configuration) configuration files.

* Starting a locked stage will update the HUD icon, but the `MISSION_OBJECTIVE_` will only appear if the player pauses.
* A stage using [SetIrisWipe](setiriswipe.md) will play the audio cue, but omit the `INGAME_MESSAGE_` popup.
