* Fixed a bug when **Independent Inputs > D-Pad Buttons** was enabled where players 2-4 could control menus with their D-Pads.
* Made the hack only tell the game about XInput devices when they're connected.
	* Also added the `-noxinputignoredisconnected`, `-noxinputmaintainorder`, `-noxinputremove` and `-noxinputadd` command line arguments to opt out of various components of this change.