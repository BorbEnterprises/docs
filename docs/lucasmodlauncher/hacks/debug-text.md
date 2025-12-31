---
title: Debug Text
description: "This hack displays various debugging information via a series of pages."
status:
    class: "wip"
---

**This is a [developer hack](all-hacks.md#developer-hacks) that can be enabled on the "Developer" page of the Mods List.**

This hack displays various debugging information via a series of pages that can be navigated with the R and T keys (or Shift+R and Shift+T for subpages).

# Configuration
Mods can customise the font Debug Text uses by loading a [Texture Font chunk](../../pure3d/chunk-types/chunk-22000.md) named `DebugText`.

# Modes
## Built-in
TODO

## Registered by Hack Support
### "hacks" Page
This page shows which hacks are enabled.

It also shows how many times they patched the game if you're using the `-testing` command line argument.

### "shared hacks" Page

**This page is only available with the [-testing](../command-line-arguments.md#testing).**

TODO

### "hack events" Page

**This page is only available with the [-testing](../command-line-arguments.md#testing).**

TODO

### "mods" Page
This page shows what mods and mod hacks are enabled.

### "keybinds" Page
This page shows what keybinds exist, what bindings they have and whether or not they're currently being pressed and whether or not they're being ignored.

### "mods" Page
This page lists all currently loaded mods and mod hacks.

## Registered by Custom Audio Support
TODO

## Registered by Custom Trigger Actions
This hack registers a mode that shows all registered conditions. While ingame, it also shows whether or not they're currently met.

## Registered by Video Texture Support
TODO

# Command Line Arguments
This hack is affected by certain [Command Line Arguments](../command-line-arguments.md#hack-debug-text) for the Mod Launcher.

# Version History
## 1.26
{{ snippet lucasmodlauncher/versions/1.26/hack_debug-text }}

## 1.25.1
{{ snippet lucasmodlauncher/versions/1.25.1/hack_debug-text }}

## 1.25
{{ snippet lucasmodlauncher/versions/1.25/hack_debug-text }}

## 1.24
{{ snippet lucasmodlauncher/versions/1.24/hack_debug-text }}

## 1.23.10
{{ snippet lucasmodlauncher/versions/1.23.10/hack_debug-text }}

## 1.23.4
### "position" Page
Made this page show all action buttons the player is in with "(main)" after the main one (the one you can interact with) instead of just showing the main one.

## 1.23.3
### "AI cars" Page
Added this page.

### "car physics objects" Page
Added this page.

### "fences" Page
Fixed an issue introduced in 1.23.2 where switching to this page broke anything that was one-sided.

## Frame Limiter
Fixed an issue where mission loading screens (used when selecting a mission or starting one) were considered menus instead of loading screens.

## 1.23.2
### General

* Added a "keyboards" page, a "mice" page and a "steering wheels" page to a new "controllers" group.
* Moved the "gamepads" page to the new "controllers" group.

### "fences" Page
Fixed a bug where this page didn't set the cull mode before rendering the fences (causing the fences to only be visible from one side in some cases).

### "mission" Page
Fixed a crash when a stage condition is null (which will crash the game when reaching the stage).

### "music" Page
Fixed a crash when using the game's "MUTE" command line argument (which is enabled by the new No Audio mod).

## 1.23.1
### General
Added a new "gamepads" debug mode.

## 1.22
### General

* Made debug class names cleaner. For example ".?AVVehicle@@" will now show up as "class Vehicle".
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

## 1.21
### "gags" Page
Added this page. It lists all the current gags (the outside ones or the ones for the current interior) and whether or not they're loading/loaded. It also shows their joint positions in the world.

## 1.20
### General
Added a "world spheres" Page that shows information about any currently loaded World Spheres and their respective Lens Flares (if applicable).

### "cars" Page
Added "Parked cars enabled" to show if parked cars are currently enabled.

### "paths" Page

* Added "Enabled" to show if pedestrians are currently enabled.
* Added "Group" to show the currently selected ped group.
* Added information about all the ped groups that exist.

## 1.19
### General

* Made Ctrl+C copy the current page text to clipboard.
    * Also added "Allow Copying with Ctrl+C" to the "Advanced" tab of the hacks settings to disable that.

### "actors" Page
Added this page.

### "cams" Page
Made this page exclude null cameras.

### "characters" Paege
Added this page.

### "intersects" Page
Made this page not say "Y: " before the Y and "Z: " before the Z of "Intersect triangle pos 3".

### "loaded characters" Page
Added this page.

### "missions" Page
Made this page exclude null missions.

### "mission" Page

* Made this page show "null" for null objectives instead of crashing.
    * This is helpful for debugging in the event the stage's objective is not getting added.

### "traffic" Page
Made this page render the segments of the road the car is currently on (and the previous roads segments if the car is on an intersection).

### "triggers" Page

* Made this page include the type number of locators in brackets after the type name.
* Made sphere triggers render as spheres now instead of boxes.

## 1.18.2
### "states and actions" Page

* Added " (no wait)" after actions that their set does not wait for.
* Added "Walker locomotion action time", "Walker locomotive action next idle animation time" and "Walker locomotive action can play idle animation"

### "lights" page
Removed "enabled" for lights and made disabled lights instead show " (disabled)" after them.

## 1.18.1
### "lights" page
Added this page.

## 1.18
### General
* Moved to the new "Developer" page.
* Added settings that allow you to configure the look and feel of the hack and which pages are visible.
* Fixed lag on the "dyna phys" and "static phys" pages while loading.
* Made the hack work during movies.
* Made the hack use Radical's official chunk names.
    * You can revert to the old names by using the new "Use Legacy Names" setting on the Advanced tab of the hack's settings.
* Made the "car joints" and "character joints" pages show the joints in the world instead of listing them.
* Made the hack check for a font called "DebugText" and use that if it exists.

### "car matrix" Page
Added this page.

### "memory" Page
Added this page with information on a few different heaps.

### "music" Page
Added this page with various information about the currently loaded RMS files.

### "regions" Page
Made this page also show the current and loaded interior.

### "road segments" Page
Added this page that draws road segments in the world with names.

### "root tree node and animated icons" Page

* Fixed a crash when going to this page when not ingame or while loading.
* Made "Animated icons" work outside the Release English version of the game.

### "traffic" Page
Made "Contact car traffic locomotion AI segment" now include the road segment name in brackets.

### "triggers" Page
Made this page list triggers the player is in and show triggers as boxes with names in the world.

## 1.17
Added this hack.