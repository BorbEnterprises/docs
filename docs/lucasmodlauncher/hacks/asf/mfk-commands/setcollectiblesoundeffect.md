---
title: SetCollectibleSoundEffect
description: "Sets the sound effect to use when collecting an item in delivery, dump or race objectives."
summary:
    initialVersion: "1.23.5"

# TODO: Fact check that this actually works on "race" objectives.

---

Sets the sound effect to use when collecting an item in [delivery](/hitandrun/scripting/objectives/delivery.md), [dump](/hitandrun/scripting/objectives/dump.md) or [race](/hitandrun/scripting/objectives/race.md) objectives.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage-objective }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCollectibleSoundEffect( sound_resource_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCollectibleSoundEffect( sound_resource_name )
```
{{ endtab }}
{{ endtabs }}

* **sound_resource_name**: The name of the sound resource to play.
    * **none**: No sound will play when picking up collectibles for the stage.
    * Default varies by level and in one case by mission:
        * Level 1: `level_1_pickup_sfx`
        * Level 2: `level_2_pickup_sfx`
        * Level 2 Mission 6: `monkey_collect`
        * Level 3: `level_3_pickup_sfx`
        * Level 4: `level_4_pickup_sfx`
        * Level 5: `level_5_pickup_sfx`
        * Level 6: `level_6_pickup_sfx`
        * Level 7: `nuclear_waste_collect`

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetCollectibleSoundEffect("W_Idlereply_Moe_genitalsA");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCollectibleSoundEffect("W_Idlereply_Moe_genitalsA")
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.23.5
Added this command.