---
title: UseTrafficGroup
description: "Set what traffic group will be used when the mission is selected or restarted."
summary:
    initialVersion: "1.22"
---

Set what traffic group will be used when the mission is selected or restarted.

# Context
{{ snippet hitandrun/command-contexts/mission-init-root }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
UseTrafficGroup( group_index );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.UseTrafficGroup( group_index )
```
{{ endtab }}
{{ endtabs }}

* **group_index**: The index of the traffic group.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");

	...

    // Use the 2nd traffic group when restarting the mission.
    // This does NOT apply when going from the SD mission into the main mission.
	UseTrafficGroup(2);

	AddStage();
    	...
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")

	...

    -- Use the 2nd traffic group when restarting the mission.
    -- This does NOT apply when going from the SD mission into the main mission.
	Game.UseTrafficGroup(2)

	Game.AddStage()
    	...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ snippet lucasmodlauncher/notes/dynamic-traffic-required }}

# Version History
## 1.22
Added this command.