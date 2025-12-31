---
title: Version 1.22
description: "This update was released on March 7th, 2019."
authors: ["loren","lucasc190"]
---

**This update was released on March 7th, 2019.**

# Highlights
## New Launcher Features

* Duplicating and exporting/importing configurations.
* Jump Lists on Windows 7 or newer.
* Various internal efficiency improvements.

## New Hacks

* Custom Traffic Support: Adds a ton of traffic related features.
* Dynamic Tree Node Entity Limits: Makes it much less tedious to modify existing maps.
* Mirror Mode: Lets you experience the game but mirrored!

## New Hack Features

* Additional Script Functionality: Two new script commands.
* Bug Fixes: Several new fixes.
* Custom Trigger Actions: Two new Action Types.
* Debug Checks: Huge improvements to various existing checks.

# Launcher
## General

* Added support for [Jump Lists](/img/lucasmodlauncher/misc/jump_list.png) on Windows 7 or newer.
    * The Jump List contains an item to Launch the game with the last configuration as well as any configurations you've enabled "Jump List" on via the Manage Configurations window. It also has an item for the Launcher's Settings.
    * Also added a `-noupdatejumplist` command line argument to prevent the Mod Launcher from updating the Jump List.
    * Also added a `-nojumplist` command line argument to clear the Jump List on startup.
* Added a `-noconfiguration` command line argument to make the Mod Launcher start on the Main configuration.
* Added a `-nounreleased` command line argument. This fully disables the Unreleased page and makes Unreleased mods appear on the other pages.
* Added a `-noedition` command line argument. This fully disables the Edition feature of mods.
* Fixed an issue where the `-nodeleteold` command line argument did not work since 1.21.
* Fixed an issue where the Mod Launcher was using the wrong number internally when deciding if "Mod compiled successfully." should be pluralised and when deciding how to format the message about a single Mod's Meta.ini having changed when launching the game or compiling a mod.
    * It was incorrectly using the amount of mods that were added with the `-mod` command line argument in both cases which is an irrelevant number.
* Made it so the Mod Launcher has an [App ID](https://docs.microsoft.com/en-us/windows/desktop/shell/appids).
    * Also added an `-appid` command line argument to use a custom App ID. This also disables updating Jump Lists.
    * Also added a `-gameappid` command line argument to make the game use the same ID as the Mod Launcher which makes them share a taskbar button.
    * Also added a `-noappid` command line argument to make it so it doesn't have one. This also disables updating Jump Lists.
    * Also added a `-updatejumplist` command line argument to opt back into updating Jump Lists when using "-appid" or "-noappid".
* Made it so the Mod Launcher goes through pinned shortcuts for the running instance (with the same arguments) on the taskbar and start menu/screen on startup and add its App ID to any that don't have one already.
    * This only applies when the Mod Launcher has an App ID.
    * Also added a "Force Update Pinned Shortcuts" option to the "Open..." menu when using the `-testing` command line argument.
    * Also added a `-forceupdatepinnedshortcuts` command line argument that makes the Mod Launcher always update pinned shortcuts even if they already have an App ID as well as when the running instance does not.
    * Also added a `-nofixpinnedshortcuts` command line argument to disable this.
* Made it so restarting the Mod Launcher with Ctrl+Shift+R or changing certain settings will retain command line arguments.
* Made it so the Main mod's icon or the Edition's icon will be used on the game window if one is enabled.
    * Also added a `-nogamemodicon` command line argument to disable this.
* Made it so Main mods that specify an Edition do not have their title before the game's name in the window title.
* Made the `-settings` command line argument include the configuration in the Settings window title when not using "-notitleconfiguration".

## Main Window

* Added a "Check for Updates" option to the "Open..." menu when using the `-testing` command line argument.
* Made the update checker show a hyperlink on the main window instead of a message box when an update is available.
    * Also added a `-updatemessage` command line argument. This restores the old update message box.
    * Also Added a `-noupdatelink` command line argument. This removes this new update hyperlink.
    * Also made the update checker get re-enabled if it was disabled in a previous version due to the fact it's now less obnoxious.

## Mods List

* Added a `-watermarkopacity` command line argument. This lets you set the opacity of the watermark in the Mods List, 0 for 0% and 1 for 100%.
* Made it so being on the Unreleased tab will not save when you close the program, instead placing you back on the General tab or the last tab you were on.
    * Also added the `-saveunreleased` command line argument to disable this.
* Made it so the "Hacks" category is available on the "Settings" and "Developer" pages when using the `-testing` command line argument.

## Mod Info
* Fixed an issue where author Websites couldn't be clicked on the Credits page.
* Fixed an issue where authors on the Credits page that were not in any groups appeared bold on Windows 7 and possibly other operating systems but seemingly not Windows 10.
* Fixed an issue where if you selected multiple mods in the same file (multiple Mod Hacks inside Hacks.dll), the size of that file was counted once for each selected mod.
* Made it so if you select one or more mods in the same file (multiple Mod Hacks inside Hacks.dll) and no mods not in that file, the name of the file they're in is shown in brackets after the size to make it more clear that it includes the entire file.

## Mod Settings

* Increased the length limit of text setting values from 63 to 127.
* Made the label of mod settings that have values set appear in bold.
    * Also added a `-noboldsettings` command line argument. This makes it so mod settings are never displayed in bold.
    * Also added a `-ignoredefaultmodsettings`command line argument. This makes it so mod settings that were manually set to their default will no longer be bold despite being set.
* Added a `-resetdefaultmodsettings` command line argument. This makes mod settings get unset when you manually put them back to their default value instead of remaining bold.
* Made it so you can right click on individual settings, groups and pages to reset them to their default value(s).
    * You can right click on the control itself and its label unless it's a textbox where you have to right click the label.
    * If you right click a setting that is disabled because of a condition then you will right click the page or group it's in and not the setting.
* Made the "Reset" button disabled if no settings have a value set.

## Launcher Settings

* Fixed an issue introduced in 1.18 where Increased Video Resolution Support and Custom Shop Support were each listed twice on the Non-mod Hacks page.
* Made it so using "-ignoremods" prevents a reload when changing Additional Mods settings.

## Account Integration

* Added a `-commsoptoutdeauthenticate` command line argument. This makes the "Deauthenticate" button fully remove your account from both the main Mod Launcher and SHAR MP.
* Changed "login" to "log in" in the window text on the old message that appears when using "-accountwindowtoken" to restore the token field.
    * This doesn't break existing language packs through the power of workarounds though the fact that this message is different as a result of the token field does.
* Fixed an issue where the window was incorrectly resized to accommodate the "Connection is not secure." text when the font was scaled (via a different DPI or the `-fontscale` command line argument).
* Fixed an issue where the window could be resized too small when showing the "Connection is not secure." text.
* Fixed an issue where the window was incorrectly centered on the main window when showing the "Connection is not secure." text.
* Made this window show the currently authenticated user's display name in brackets after their username in the "Username" field.
* Removed the Token field.
    * Also added a `-accountwindowtoken` command line argument to restore this field.

## Configurations

* Added the ability to duplicate configurations.
* Added the ability to export and import configurations.
* Added the ability to add configurations to the Jump List.
* Made configurations have the icon of the Main mod enabled in them or the icon of the Edition enabled in them.
    * These are shown in place of the Mod Launcher's icon on the window, on the configurations list and in the Jump List.
* Made the "Main" configuration listed on the "Manage Configurations..." window. It is not deletable or renamable.

## Localization
This version introduces several new language strings that language packs will need to be updated to include. These pertain to the new update hyperlink and the new features of the Manage Configurations window.

A new template language (Template_1.22.xml) was published on [this page](../localisation.md) including this new language strings at the end of the file.

# Mod Features

* Added new `[Description]` sections that allow mods to split up their description into multiple headers on their About page.
* Added a `Testing` property to `[Setting]` sections that disables them and any conditions relating to them when not using the `-testing` command line argument.

# Mods
## Never Busted
Added this new mod.

## No License Screen Delay.
Added this new mod.

# Hacks
## General

* Added various new asserts when using the `-testing` command line argument.
* Completely re-wrote the underlying file system that powers all of the hacks to be considerably more efficient.
    * Also added a `-nofilesystem` command line argument. This fully disables the Mod Launcher's virtual filesystem making it basically unusable as far as launching the game goes.
    * Also added a `-legacyfilesystem` command line argument. This makes the Mod Launcher use its old virtual filesystem instead of this new one.
* Fixed a crash when returning to the main menu from demo gameplay (accessible with various hacks such as Debug Test or Skip Main Menu).
    * It will still crash if you exit the game during the demo.
* Made debug class names used by Debug Text and various other hacks cleaner. For example ".?AVVehicle@@" will now show up as "class Vehicle".

## Additional Script Functionality
### General

* Fixed an issue introduced in 1.21 where there would be an assert when entering the bonus game.
* Made characters added to cars with ASF commands get removed from and re-added to the world when the car does instead of just when it explodes and is repaired.
    * Characters also now only get added immediately if the car is already in the world.
    * This resolves an issue where characters could remain floating in the air after the game removed a car.
* Made `g_CustomMissionData.empty()` only assert when using the `-testing` command line argument.

### MFK Commands

* Added `AddParkedCar`. This allows you to add a car to the level's parked cars list without needing it to be also added to a traffic group with AddTrafficModel.
* Added `UseTrafficGroup`. This sets the current traffic group index when getting to the mission via mission select or restarting it. This does not work unless the DynamicTraffic feature of CustomTrafficSupport is set to `Models` or `Slots`.

## Bug Fixes

* Added "Vehicles > No Air Vent Audio".
    * Also added a `NoAirVentAudio` property to the `[Vehicles]` section of BugFixes.ini.
* Added "Crashes > Car Deleted While Loading CON File" when using "-testing".
    * Also added a `FixCarDeletedWhileLoadingCONFileCrash"` to the `[Crashes]` section of BugFixes.ini since mods are intended to opt into this.
* Added "Crashes > Zone Load on Exit" when using "-testing".
    * Also added a `FixZoneLoadOnExitCrash` to the `[Crashes]` section of BugFixes.ini since mods are intended to opt into this.

## Console
Made the title of the console window "Lucas' Simpsons Hit & Run Mod Launcher Console" instead of the path to the game.

## Cheat Keys
Made F4 (or Shift+F4 if you already have a car like you're always supposed to unless you're playing SHAR MP) show the phone booth.

## Custom Audio Support
Added support for a `Number` attributes on `<Level>` and `<Mission>` elements.

## Custom Car Support

* Added the `-nocarindexmapping` command line argument. This disables the hack re-mapping car indices.
* Fixed an issue preventing Car Camera Data index remapping from working for cars loaded from a Mod's Resources folder (and possibly other locations).

## Custom Files
### General

* Added the `-noadditionalfiles` command line argument. This disables the AdditionalFiles functionality of this hack which will break mods that rely on it.
* Added the `-slowgameload` command line argument. This allows you to artificially increase load times.
* Made this hack only handle requesting a file when necessary.
* Made this hack generate a list of mods that have AdditionalFiles folders on startup and only check those mods when a file is requested instead of every mod.

### Lua Scripting

* Added "GetModTitle". This returns the current mod's title (or the title of the specified mod if one is specified).
* Added "GetModVersion". This returns the current mod's version (or the version of the specified mod if one is specified).

## Custom Limits

* Added `CarLimit` and `ActionButtonLimit` to the `[Miscellaneous]` section.
* Added a `[CollisionIndices]` section that lets you increase the limit on various types of collision indices.
    * No longer will Lucas sing about there not being [enough collision indices](https://youtu.be/iiIkcr83J9I?t=133).
* Added a `[Sound]` section that lets you increase `PlayingClipPlayerLimit` and `PlayingStreamPlayerLimit`.
* Made this hack assert if the `Limit` in the `[Regions]` section was set to more than 127.

## Custom Road Behaviour
Added support for a `Number` attribute on `<Level>` elements.

## Custom Traffic Support
Added this new hack that allows you to have dynamic traffic groups, more than 5 traffic cars, custom traffic colors and more.

## Custom Trigger Actions

* Added a `ChangeTrafficGroup` action. This allows you to set the current traffic group with any trigger. This does effectively nothing unless DynamicTraffic is enabled in CustomTrafficSupport.
* Added a `TriggerMusicEvent` action. This allows you to trigger any music event in the current music RMS file with any trigger.
    * Due to various ways the game handles music, this might not be very practical but it's there!

## Custom Shop Support
Added support for a `SkinShop` element in this hack's configuration file that works similarly to the existing `PhoneBooth` element.

## Debug Checks

* Added "Experimental Missing Detection > Composite Drawable" to detect when a composite drawable is missing in cases where that matters.
* Moved "Experimental Missing Locator Detection" to the new "Experimental Missing Detection" group and renamed it accordingly.
* Made exceeding tree node entity limits get detected immediately instead of the next frame (when the game may have already crashed) and made the limit get increased on the fly instead of corrupting the game.
    * If multiple limits are exceeded during a set of zones being loaded (such as when hitting a load zone or selecting/restarting a mission), a single message is shown by default though this can be disabled by unticking "Combine Zone Tree Node Exceeded Messages".

## Debug Test
### General

* Made it only check if the "H" key is down once each frame instead of once for every possible collision.
* Made it only check if the "H" key is down when the game window is focused.
* Made the vehicle controller used when possessing vehicles with the 8 key only get the key states once each frame.
    * Did you know about this feature? We didn't.
* Made possessing vehicles with the 8 key still use their old controller when not accelerating or steering, not switch them to in-car physics until accelerating or steering and take traffic cars off rails when not accelerating or steering.
    * No seriously, Lucas found out he did this recently. I wonder what other secrets there are...
    * Loren should really document Debug Test sometime.

### Graphics Page

* Added "Software Vertex Processing".
* Added "Flip > X", "Flip > Y", "Flip > Z" and "Flip > Cull Mode" to flip the viewport in wacky ways.

### Vehicles Page

* Added "Air Vent Force". Now your car can soar like a candy wrapper in an updraft.
    * This suppresses the new "Vehicles > No Air Vent Audio" feature of Bug Fixes if the force is not 0.
* Added "Override Maximum Traffic".
* Added "No Load Properties" to disable the game loading CON files.
    * Also added "Set Up Vehicle Handling" and "Create Driver" to make the game do some initialization stuff it would've done if it loaded the CON file.
* Removed the limit of 5 on "Vehicles > Road Nodes > Maximum Cars".

### Miscellaneous Page

* Added "Gravity" settings. Far out!
    * Screen might go blue if you set some of these numbers the wrong way. No warranty included.
* Added "Heaps > No Temp Heap".
* Moved "Use Tracking Heaps" into the new "Heaps" group.

## Debug Text
### General

* Added a `-debugtextmode` command line argument. This can be used to launch the game with a specific debug mode enabled.
* Added a `-noscaledebugtext` command line argument. This disables the debug text being scaled according to the size of the window.
* Made the debug text scale down to fit the screen.
    * Also added a `-nofitdebugtext` command line argument to disable this.
* Made it so pages that are not built in are grouped by what Mod/Hack added them.
    * Grouped pages can be cycled by holding Shift+T/Shift+R.
    * Also added a `-nodebugtextgroups` command line argument to disable this.
* Made the "traffic" and "road segments" pages show intersections as blue spheres in the world as well as their names.
* Removed the "root tree node and animated icons" page and moved its contents to the "tree" and "miscellaneous" pages respectively.

### "miscellaneous" Page

* Added "Action buttons" to show the amount of action buttons that exist out of the maximum.
* Added "Playing sound clip players" and "Playing sound stream players" which show the current amounts out of the maximums.

### "cars" Page

* Added "Parked car count" to show how many parked cars currently exist.
* Moved the listed traffic cars to the "traffic" page.

### "mission" Page

* Now shows "Time" in stages with a timer. This is shown in milliseconds.
* Now shows the current time and duration on "timer" objectives in milliseconds.

### "traffic" Page

* Added "Count" to show the amount of traffic cars currently in existence out of the maximum.
* Added "In-car limit" to show what the in-car limit is currently set to.
* Added "Group" to show what traffic group is currently in use.
* Added a list of all models in the current traffic group with the current amount of each one out of their maximum.
* Added a list of all current traffic cars and whether or not they're active (in the world).

### "music" Page
Fixed a crash when viewing this page when the current region had multiple layers in it.

### "paths" Page

* Made this page only show the models of the current ped group and not show an "x" after each count.
* Made this page show characters and which ones are in use.

## Discord Rich Presence

* Added the "RapidJSON" license.
* Made this hack output `DISCORD RICH PRESENCE: Initialising...` when initialising Discord RPC.
* Made this hack wait until the main menu to initialise Discord RPC.
    * This seems to make the hack work far more reliably than before.

## Dynamic Tree Node Entity Limits
Added this new hack. This makes tree node entity limits get adjusted dynamically if any get exceeded which removes the need to manually increase them.

## Frame Limiter
Made the loading screen used when returning to the main menu or going to the Bonus Game menu from the main menu uncapped when "Limit > While on Loading Screens" is disabled but not when "Limit > While on Menus" is disabled.

## Hack Support
* Added a new "mods" page when Debug Text is enabled. This page lists all mods and mod hacks that are enabled.
* Added a `-nounrequesthackevents` command line argument. This makes it so hacks do not unrequest hack events they're not using after the first time they're told about them resulting in reduced efficency.
* Added a `-nohookd3d` command line argument. This disables the Mod Launcher hooking D3D and breaks functionality of numerous hacks. Fun!
* Added new "hacks", "shared hacks" and "hack events" pages that show up in Debug Text when using the `-testing` command line argument.
* Made the `-suspend` command line argument show its message earlier.
* Made the `-testing` command line argument show an assert if the game gets terminated because it took more than 1 second to exit.
* Made it so this hack only installs shared patches when they are necessary.
    * Also added "-installallsharedhacks". This makes all shared patches get installed regardless of whether or not they're actually in use.
* Made this hack show an assert if it tries to patch the game, call game code or read/write variables if there is no address for the current game version.
    * In the case of patches, the patch is also not applied. Otherwise, the game will probably crash after the assert.
    * This should never happen, probably.
    * Anyways, you can use "-ignoremissingaddresses" to disable this assert.

## Increased Reward Limits
Added support for an INI file that allows you to increase the limit of Car and Skin previews to custom amounts. Now Multi-Meme can have more cars!

## No Time Limits
Added settings to this hack for whether or not it affects Mission Timers and Timer Objectives instead of just affecting Mission Timers always.

## Mirror Mode
Added this new hack that flips the viewport of the world.

## NVIDIA Highlights
Added a new "Air Vent" type of highlight. This is disabled by default because your air vent trick shots are not cool.

## Screenshots
Made it so holding the F12 key will no longer rapidly take screenshots. Also added a `-continuousscreenshots` command line argument to undo this.

## Skip Main Menu

* Added "Bonus Game" to load directly into the awesome Bonus Game. 
    * If you have no bonus game levels unlocked, the bonus game will become fully unlocked until you return to the main menu.
* Added "Demo" to load directly into the selected Level's demo when using "-testing".
* Made changing the "Level" away from "1" not set a value for "Mission".
* Made the newspaper sound attempt to play.