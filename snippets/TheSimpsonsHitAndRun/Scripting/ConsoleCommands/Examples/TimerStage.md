{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1sd");
	// ...

	// Simple timer stage as the final stage in a Sunday Drive mission
	// Do not use final in these missions!
	AddStage();
		AddObjective("timer");
			SetDurationTime(1);
		CloseObjective();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1sd")
	-- ...

	-- Simple timer stage as the final stage in a Sunday Drive mission
	-- Do not use final in these missions!
	Game.AddStage()
		Game.AddObjective("timer")
			Game.SetDurationTime(1)
		Game.CloseObjective()
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}