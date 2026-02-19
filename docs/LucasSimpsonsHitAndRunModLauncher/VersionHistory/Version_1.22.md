---
title: "Version 1.22"
description: "Changelog for Version 1.22 of Lucas' Simpsons Hit & Run Mod Launcher."
authors: [ 2 ]
---

**This version was released on March 7, 2019.**

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
* Added support for Jump Lists on Windows 7 or newer.
    * The Jump List contains an item to Launch the game with the last configuration as well as any configurations you've enabled **Jump List** on via the Manage Configurations window. It also has an item for the Launcher's Settings.
    * Also added a `-noupdatejumplist` command line argument to prevent the Mod Launcher from updating the Jump List.
    * Also added a `-nojumplist` command line argument to clear the Jump List on startup.
* Added a `-noconfiguration` command line argument to make the Mod Launcher start on the Main configuration.
* Added a `-nounreleased` command line argument. This fully disables the Unreleased page and makes Unreleased mods appear on the other pages.
* Added a `-noedition` command line argument. This fully disables the Edition feature of mods.
* Fixed an issue where the `-nodeleteold` command line argument did not work since 1.21.
* Fixed an issue where the Mod Launcher was using the wrong number internally when deciding if **Mod compiled successfully.** should be pluralised and when deciding how to format the message about a single Mod's Meta.ini having changed when launching the game or compiling a mod.
    * It was incorrectly using the amount of mods that were added with the `-mod` command line argument in both cases which is an irrelevant number.
* Made it so the Mod Launcher has an [App ID](https://docs.microsoft.com/en-us/windows/desktop/shell/appids).
    * Also added an `-appid` command line argument to use a custom App ID. This also disables updating Jump Lists.
    * Also added a `-gameappid` command line argument to make the game use the same ID as the Mod Launcher which makes them share a taskbar button.
    * Also added a `-noappid` command line argument to make it so it doesn't have one. This also disables updating Jump Lists.
    * Also added a `-updatejumplist` command line argument to opt back into updating Jump Lists when using `-appid` or `-noappid`.
* Made it so the Mod Launcher goes through pinned shortcuts for the running instance (with the same arguments) on the taskbar and start menu/screen on startup and add its App ID to any that don't have one already.
    * This only applies when the Mod Launcher has an App ID.
    * Also added a **Force Update Pinned Shortcuts** option to the **Open...** menu when using the `-testing` command line argument.
    * Also added a `-forceupdatepinnedshortcuts` command line argument that makes the Mod Launcher always update pinned shortcuts even if they already have an App ID as well as when the running instance does not.
    * Also added a `-nofixpinnedshortcuts` command line argument to disable this.
* Made it so restarting the Mod Launcher with Ctrl+Shift+R or changing certain settings will retain command line arguments.
* Made it so the Main mod's icon or the Edition's icon will be used on the game window if one is enabled.
    * Also added a `-nogamemodicon` command line argument to disable this.
* Made it so Main mods that specify an Edition do not have their title before the game's name in the window title.
* Made the `-settings` command line argument include the configuration in the Settings window title when not using `-notitleconfiguration`.

## Main Window
* Added a **Check for Updates** option to the **Open...** menu when using the `-testing` command line argument.
* Made the update checker show a hyperlink on the main window instead of a message box when an update is available.
    * Also added a `-updatemessage` command line argument. This restores the old update message box.
    * Also Added a `-noupdatelink` command line argument. This removes this new update hyperlink.
    * Also made the update checker get re-enabled if it was disabled in a previous version due to the fact it's now less obnoxious.

## Mods List
* Added a `-watermarkopacity` command line argument. This lets you set the opacity of the watermark in the Mods List, 0 for 0% and 1 for 100%.
* Made it so being on the Unreleased tab will not save when you close the program, instead placing you back on the General tab or the last tab you were on.
    * Also added the `-saveunreleased` command line argument to disable this.
* Made it so the **Hacks** category is available on the **Settings** and **Developer** pages when using the `-testing` command line argument.

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
* Made the **Reset** button disabled if no settings have a value set.

## Launcher Settings
* Fixed an issue introduced in 1.18 where Increased Video Resolution Support and Custom Shop Support were each listed twice on the Non-mod Hacks page.
* Made it so using `-ignoremods` prevents a reload when changing Additional Mods settings.

## Account Integration
* Added a `-commsoptoutdeauthenticate` command line argument. This makes the **Deauthenticate** button fully remove your account from both the main Mod Launcher and SHAR MP.
* Changed **login** to **log in** in the window text on the old message that appears when using `-accountwindowtoken` to restore the token field.
    * This doesn't break existing language packs through the power of workarounds though the fact that this message is different as a result of the token field does.
* Fixed an issue where the window was incorrectly resized to accommodate the **Connection is not secure.** text when the font was scaled (via a different DPI or the `-fontscale` command line argument).
* Fixed an issue where the window could be resized too small when showing the **Connection is not secure.** text.
* Fixed an issue where the window was incorrectly centered on the main window when showing the **Connection is not secure.** text.
* Made this window show the currently authenticated user's display name in brackets after their username in the **Username** field.
* Removed the Token field.
    * Also added a `-accountwindowtoken` command line argument to restore this field.

## Configurations
* Added the ability to duplicate configurations.
* Added the ability to export and import configurations.
* Added the ability to add configurations to the Jump List.
* Made configurations have the icon of the Main mod enabled in them or the icon of the Edition enabled in them.
    * These are shown in place of the Mod Launcher's icon on the window, on the configurations list and in the Jump List.
* Made the **Main** configuration listed on the **Manage Configurations...** window. It is not deletable or renamable.

## Localization
This version introduces several new language strings that language packs will need to be updated to include. These pertain to the new update hyperlink and the new features of the Manage Configurations window.

A new template language (Template_1.22.xml) was published on [Project:181] including these new string formats as well as the original strings. The template also now indicates when strings were removed if they were in this update or any previous ones.

# Mod Features
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/ModFeatures.md }}

# New Mods
## Never Busted
Added this new mod.

## No License Screen Delay.
Added this new mod.

# New Hacks
## Custom Traffic Support
Added this new hack that allows you to have dynamic traffic groups, more than 5 traffic cars, custom traffic colors and more.

## Dynamic Tree Node Entity Limits
Added this new hack. This makes tree node entity limits get adjusted dynamically if any get exceeded which removes the need to manually increase them.

## Mirror Mode
Added this new hack that flips the viewport of the world.

# Updated Hacks
## General
* Added various new asserts when using the `-testing` command line argument.
* Completely re-wrote the underlying file system that powers all of the hacks to be considerably more efficient.
    * Also added a `-nofilesystem` command line argument. This fully disables the Mod Launcher's virtual file system making it basically unusable as far as launching the game goes.
    * Also added a `-legacyfilesystem` command line argument. This makes the Mod Launcher use its old virtual file system instead of this new one.
* Fixed a crash when returning to the main menu from demo gameplay (accessible with various hacks such as Debug Test or Skip Main Menu).
    * It will still crash if you exit the game during the demo.
* Made debug class names used by Debug Text and various other hacks cleaner. For example `.?AVVehicle@@` will now show up as `class Vehicle`.

## Hack Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/HackSupport.md }}

## Additional Script Functionality
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/AdditionalScriptFunctionality.md }}

## Bug Fixes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/BugFixes.md }}

## Cheat Keys
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CheatKeys.md }}

## Console
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/Console.md }}

## Custom Audio Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CustomAudioSupport.md }}

## Custom Car Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CustomCarSupport.md }}

## Custom Files
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CustomFiles.md }}

## Custom Limits
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CustomLimits.md }}

## Custom Road Behaviour
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CustomRoadBehaviour.md }}

## Custom Shop Support
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CustomShopSupport.md }}

## Custom Trigger Actions
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/CustomTriggerActions.md }}

## Debug Checks
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/DebugChecks.md }}

## Debug Test
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/DebugTest.md }}

## Debug Text
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/DebugText.md }}

## Discord Rich Presence
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/DiscordRichPresence.md }}

## Frame Limiter
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/FrameLimiter.md }}

## Increased Reward Limits
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/IncreasedRewardLimits.md }}

## No Time Limits
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/NoTimeLimits.md }}

## NVIDIA Highlights
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/NVIDIAHighlights.md }}

## Screenshots
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/Screenshots.md }}

## Skip Main Menu
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.22/Hacks/SkipMainMenu.md }}