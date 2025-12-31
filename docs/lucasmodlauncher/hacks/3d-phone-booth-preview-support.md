---
title: 3D Phone Booth Preview Support
description: "This hack allows mods to have 3D previews in the phone booth in place of the usual 2D sprites."
---

**This hack must be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

This hack allows mods to have 3D previews in the phone booth in place of the usual 2D sprites.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=3DPhoneBoothPreviewSupport
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `3DPhoneBoothPreviewSupport.ini` and add the parameters necessary for your mod inside it.

```ini
; [Miscellaneous] Section
	; BackgroundPath: The path to the background scene that will be loaded for the 3D Phonebooth.
		; Defaults to art\\frontend\\scrooby\\resource\\pure3d\\rewardbg.p3d.
	; DarkenLockedCars: Set whether or not locked cars should be dark in color.
		; Defaults to 0.
	; FullScreen: Set whether or not the scene should be fullscreen.
		; Defaults to 1.
	; Radius: Set the size of the cars on the pedestal.
		; Defaults to 3.6.
	
[Miscellaneous]
BackgroundPath=art\\frontend\\scrooby\\resource\\pure3d\\rewardbg.p3d
DarkenLockedCars=0
FullScreen=1
Radius=3.6
```

# Using This Hack
This hack requires changes to the frontend file `art\frontend\scrooby\ingame.p3d` to function. Requiring this hack in a mod without making these changes will cause a crash when opening phone booths.

The specific changes involve adding the chunks highlighted in the image below to `Phonebooth.pag`.

![frontend changes](/img/lucasmodlauncher/hacks/3d-phone-booth-preview-support/frontend-changes.png)

We distribute a mod called [3D Phone Booth Previews](https://modbakery.donutteam.com/releases/view/15) that utilizes this hack and makes these necessary changes. It also re-configures the hack to fit its specific implementation of the feature. If you want to implement this feature into your mod you have a few options:

* Mods that do not modify `art\frontend\scrooby\ingame.p3d` should be compatible with the [3D Phone Booth Previews](https://donutteam.com/downloads/3DPhoneBooth) mod right away.
* Mods that do modify this file can copy the aforementioned chunks into their copy of it and add `SupportedMod=3DPhoneBoothPreviews` to the `[Miscellaneous]` section of their `Meta.ini` to add support for being enabled alongside that mod.
* Mods can force this feature on by copying the chunks, requiring the hack and copying `3DPhoneBoothPreviewSupport.ini` from 3D Phone Booth Previews.

Mods will also need to provide car shop preview models in `art\frontend\dynaload\cars` for any custom cars.

# Version History
## 1.18.2
Made the game assert when loading if `Phonebooth.pag` in "art\frontend\scrooby\ingame.p3d" is missing the `PreviewWindow`, `RewardFG` or `RewardBG` frontend elements required for the hack to work.

## 1.18.1

* Fixed an issue when not using `DarkenLockedCars` where all cars in the phone booth would appear dark after closing and opening it.
* Fixed interference between the lights in the phone booth and the lights in the car shop.

## 1.18
Added this hack.