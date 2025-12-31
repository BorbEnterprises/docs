---
title: BindReward
description: Binds a reward car or skin to a level with a specific quest type.
authors: ["loren"]
---

This command binds a reward car or skin to a level with a specific quest type.

# Context
{{ snippet hitandrun/command-contexts/rewards }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
BindReward( name, path, reward_type, quest_type, level, [price, seller] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.BindReward( name, path, reward_type, quest_type, level, [price, seller] )
```
{{ endtab }}
{{ endtabs }}

* **name**: The internal name of the reward car or skin.
	* For example, `famil_v` is the internal name of the family sedan.
* **path**: The path to the file containing the reward car or skin.
	* Note that skin file names only include the first 6 characters of the skin's internal name.
	* This would mean the skin `b_military` has the file name `b_mili_m.p3d`.
* **reward_type**: The type of reward.
	* `car` or `skin`.
* **quest_type**: The quest type required to get the reward.
	* For `car` type rewards you can use:
		* `defaultcar`
		* `forsale`
		* `bonusmission`
		* `streetrace`
	* For `skin` type rewards you can use:
		* `defaultskin`
		* `forsale`
* **level**: The level this reward is in.
	* Anywhere from 1 to 7.
* **price**: Specify the price for a `forsale` quest type reward.
* **seller**: Specify the seller of a `forsale` quest type reward.
	* For `car` type rewards you can use:
		* `gil` for Gil.
		* `simpson` for the other seller which varies from level to level.
	* For `skin` type rewards you must use `interior`.

# Examples
## Car Rewards {{ id cars }}
{{ tabs }}
{{ tab MFK }}
```text
BindReward("famil_v", "art\cars\famil_v.p3d", "car", "defaultcar", 1);
BindReward("cletu_v", "art\cars\cletu_v.p3d", "car", "bonusmission", 1);
BindReward("elect_v", "art\cars\elect_v.p3d", "car", "streetrace", 1);
BindReward("plowk_v", "art\cars\plowk_v.p3d", "car", "forsale", 1, 150, "simpson");
BindReward("cDuff", "art\cars\cDuff.p3d", "car", "forsale", 1, 125, "gil");
BindReward("cVan", "art\cars\cVan.p3d", "car", "forsale", 1, 100, "gil");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.BindReward("famil_v", "art\\cars\\famil_v.p3d", "car", "defaultcar", 1)
Game.BindReward("cletu_v", "art\\cars\\cletu_v.p3d", "car", "bonusmission", 1)
Game.BindReward("elect_v", "art\\cars\\elect_v.p3d", "car", "streetrace", 1)
Game.BindReward("plowk_v", "art\\cars\\plowk_v.p3d", "car", "forsale", 1, 150, "simpson")
Game.BindReward("cDuff", "art\\cars\\cDuff.p3d", "car", "forsale", 1, 125, "gil")
Game.BindReward("cVan", "art\\cars\\cVan.p3d", "car", "forsale", 1, 100, "gil")
```
{{ endtab }}
{{ endtabs }}

# Skin Rewards {{ id skins }}
{{ tabs }}
{{ tab MFK }}
```text
BindReward("homer", "art\chars\homer_m.p3d", "skin", "defaultskin", 1);
BindReward("h_undrwr", "art\chars\h_undr_m.p3d", "skin", "forsale", 1, 100, "interior");
BindReward("h_fat", "art\chars\h_fat_m.p3d", "skin", "forsale", 1, 125, "interior");
BindReward("h_stcrobe", "art\chars\h_stcr_m.p3d", "skin", "forsale", 1, 150, "interior");
```
{{ endtab }}
{{ tab Lua }}
```lua
BindReward("homer", "art\\chars\\homer_m.p3d", "skin", "defaultskin", 1);
BindReward("h_undrwr", "art\\chars\\h_undr_m.p3d", "skin", "forsale", 1, 100, "interior");
BindReward("h_fat", "art\\chars\\h_fat_m.p3d", "skin", "forsale", 1, 125, "interior");
BindReward("h_stcrobe", "art\\chars\\h_stcr_m.p3d", "skin", "forsale", 1, 150, "interior");
```
{{ endtab }}
{{ endtabs }}


# Notes
By default, there are various limitations related to binding rewards.

Mods can bypass these limits by requiring the [Mod Launcher's](/lucasmodlauncher/intro.md) [Increased Reward Limits](/lucasmodlauncher/hacks/increased-reward-limits.md) hack.