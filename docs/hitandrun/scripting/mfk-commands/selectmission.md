---
title: SelectMission
description: "Sets what mission is about to be initialised."
authors: ["loren"]
---

This command sets what mission is about to be initialised.

# Context
{{ snippet hitandrun/command-contexts/mission-init }}

Additionally, this must be followed by a call to [SetMissionResetPlayerInCar](setmissionresetplayerincar.md) *or* [SetMissionResetPlayerOutCar](setmissionresetplayeroutcar.md), a call to [SetDynaLoadData](setdynaloaddata.md), at least one stage and finally a call to [CloseMission](closemission.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SelectMission( mission );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission( mission )
```
{{ endtab }}
{{ endtabs }}

* **mission**: The ID of the mission that's about to be initialised.

# Examples
{{ snippet hitandrun/mfk-commands/selectmission-closemission-example }}

# Notes
No additional notes.