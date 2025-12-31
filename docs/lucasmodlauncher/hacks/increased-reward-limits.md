---
title: Increased Reward Limits
description: "This hack increases some reward related limits when it's required as well as being configurable for some more advanced limits."
---

**This hack can be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

This hack increases some reward related limits when it's required as well as being configurable for some more advanced limits.

# Limits
This table indicates what reward related limits exist in the original game and what they're increased to with this hack.

| Limit                                                 | Original Limit | Increased Limit              |
|-------------------------------------------------------|----------------|------------------------------|
| Maximum "forsale" Rewards Per Level in the Saved Game | 12             | Infinite                     |
| Maximum "forsale" Rewards Per Level                   | 8              | Infinite                     |
| Maximum Skins in Skin Shops                           | 4              | Defaults to 64, Configurable |
| Maximum Cars in the Phonebooth and Car Shops          | 64             | Defaults to 64, Configurable |
| Maximum Car Health Values in Save Data                | 60             | Not Increased                |
| Maximum Car Attributes                                | 50             | Infinite                     |

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=IncreasedRewardLimits
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `IncreasedRewardLimits.ini` and add the parameters necessary for your mod inside it.

```ini
; IncreasedRewardLimits.ini
	; Increase some more advanced limits that must be set to an exact number.
	
; [Previews] Section
	; CarLimit: The maximum amount of cars that can be in skin shop or a phonebooth. 
        ; Defaults to 64.
	; SkinLimit: The maximum amount of skins that can be in skin shops. 
        ; Defaults to 64 with this hack enabled and 4 without it.
        ; This is because the hack used to simply increase this limit to 64 by default.

[Previews]
CarLimit=64
SkinLimit=64
```

# Version History
## 1.22
Added the ability to configure the car and skin limits with `IncreasedRewardLimits.ini`

## 1.18

* Made it so the game won't get corrupt when trying to add more than 60 car health values to the save file. It now shows an assert message when trying to add more than 60 (except for when the mod is being used in Multiplayer).
* Removed the assert when trying to add more than 60 reward cars.
* Removed the limit of 64 reward cars.
    * **NOTE:** There is still a limit of 64 cars in one phonebooth but you can use CustomShopSupport to spread the cars across multiple phonebooths.

## 1.17
Added this hack.