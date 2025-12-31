---
title: CloseMission
description: "Closes a mission that was being initialised."
authors: ["loren"]
---

This command closes a mission that was being initialised.

# Context
{{ snippet hitandrun/command-contexts/mission-init }}

Additionally, this must be preceded by a call to [SelectMission](selectmission.md), [SetMissionResetPlayerInCar](setmissionresetplayerincar.md) *or* [SetMissionResetPlayerOutCar](setmissionresetplayeroutcar.md), a call to [SetDynaLoadData](setdynaloaddata.md) and at least one stage.

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ snippet hitandrun/mfk-commands/selectmission-closemission-example }}

# Notes
No additional notes.