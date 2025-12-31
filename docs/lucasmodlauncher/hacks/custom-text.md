---
title: Custom Text
description: "This hack allows mods to specify custom text strings globally as well as on a per level and per mission basis."
---

**This hack must be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

This hack allows mods to specify custom text strings globally as well as on a per level and per mission basis.

# Folder
This hack's configuration files can be placed in a folder named "CustomText". This allows for a mod's text to be localised into various languages.

If a mod provides 2 or more Custom Text configuration files in this folder, a special "Language" setting will appear in the mod's settings.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomText
```

Your mod must provide at least one configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomText.ini` or a configuration file in a `CustomText` folder and add the parameters necessary for your mod inside it.

```ini
; [Miscellaneous] Section: Other settings.
	; Title: Set the title displayed in the Language setting when using multiple CustomText files in CustomText folder.
	
; [Variables] Section: Define variables for use in Custom Text strings.
	; VARIABLE_NAME=VARIABLE_CONTENTS

	; Variables can use any other variables defined before them in the file.
	; The hack processes all of these sections before any other section in the file 
	;	so CustomText sections can use variables defined after them.
	; Variable names can only be defined once per CustomText file and an assert will be shown if one appears multiple times.

	; Variables are referenced by putting their name inside () with a $ before it, for example: $(MyCoolVariable)

	; The Mod Launcher provides some default variables as well, these CAN be overriden by mods.
	;	$(ModName): Inserts the title of the Mod using this CustomText.
	;	$(ModVersion): Inserts the version of the Mod using this CustomText.

	; This section can be repeated.

; [CustomText] Section: Global Text Strings
; [CustomTextLX] Section: Per Level Text Strings
; [CustomTextLXMX] Section: Per Story Mission Text Strings
; [CustomTextLXSRX] Section: Per Street Race Text Strings
; [CustomTextLXGR1] Section: Per Gamble (Wager) Race Text Strings
; [CustomTextLXBM1] Section: Per Bonus Mission Text Strings
	; STRING_NAME: Change the text of the specified string by name. Repeat for each string.

	; These sections can be repeated.

; Notes
	; You can find the names of text strings by enabling the Text Names mod shipped with the Mod Launcher and opening the game.
	; You can also find them by looking around in frontend files.

[Miscellaneous]
Title=English

[Variables]
DankPrefix=Dank
FamilySedanName=Pink Vehicle

[CustomText]
; Use the two variables defined above
FAMIL_V=$(DankPrefix) $(FamilySedanName)

; Car named after the mod for some reason
BART_V=$(ModName)

; String with no variables
LISA_V=Malibooooo Kar

[CustomTextL1]
MISSION_FAILED=DO'H!

[CustomTextL1M3]
MISSION_OBJECTIVE_01=AVOID BARNEY.
MISSION_OBJECTIVE_02=AVOID BARNEY 2: ELECTRIC BOOGALOO.

[CustomTextL1SR1]
MISSION_OBJECTIVE_01=FINISH THE RACE IN FIRST, OR ELSE!
```

# Version History
## 1.26
{{ snippet lucasmodlauncher/versions/1.26/hack_custom-text }}

## 1.23.8
Added support for defining variables and using them in text strings.

## 1.22.1
Removed this hack's length limit on strings, instead using the general limit (now 32767).

## 1.15.2
Fixed a crash that sometimes occurred while automatically loading the most recent saved game.

## 1.2 or earlier
Added this hack.