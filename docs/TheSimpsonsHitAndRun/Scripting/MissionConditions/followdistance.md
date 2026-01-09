---
title: "followdistance"
description: "Fail the player if they go beyond a certain distance from an AI vehicle."
authors: [ 2116 ]
---

Fail the player if they go beyond a certain distance from an AI vehicle.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("followdistance");
	// Required: Specify the distance the player needs to be in order to fail. Only the second value is used, the first value is always treated as 0.
	SetFollowDistances(0, 250);
  
	// Required: Specify which vehicle the player needs to stay close to.
	SetCondTargetVehicle("cVan");
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("followdistance")
	-- Required: Specify the distance the player needs to be in order to fail. Only the second value is used, the first value is always treated as 0.
	Game.SetFollowDistances(0, 250)
	
	-- Required: Specify which vehicle the player needs to stay close to.
	Game.SetCondTargetVehicle("cVan")
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
This condition isn't limited to [[../MissionObjectives/follow.md]] objectives, it can also be used with any other objective so long as an AI vehicle is present.

Do note, however, that when used with a [[../MissionObjectives/losetail.md]] objective, the game will only render a single bar that constantly switches between the distance of the followdistance condition and the losetail objective.