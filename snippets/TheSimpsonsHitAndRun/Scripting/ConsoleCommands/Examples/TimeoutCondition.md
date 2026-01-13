{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	AddStage();
		SetStageTime(10);

		AddObjective("dummy");
		CloseObjective();

		// Fail the player if they take longer than 10 seconds on this stage
		AddCondition("timeout");
		CloseCondition();
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.SetStageTime(10)

	Game.AddObjective("dummy")
	Game.CloseObjective()

	-- Fail the player if they take longer than 10 seconds on this stage
	Game.AddCondition("timeout")
	Game.CloseCondition()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}