---
title: SetNoHitAndRunMusicForStage
description: "Disables the game switching to the Hit & Run music during a Hit & Run for the stage. Instead, the mission's music will continue."
summary:
    initialVersion: "1.18"
---

Disables the game switching to the Hit & Run music during a Hit & Run for the stage. Instead, the mission's music will continue.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetNoHitAndRunMusicForStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetNoHitAndRunMusicForStage()
```
{{ endtab }}
{{ endtabs }}



# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	SetNoHitAndRunMusicForStage();

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.SetNoHitAndRunMusicForStage()

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18
Added this command.