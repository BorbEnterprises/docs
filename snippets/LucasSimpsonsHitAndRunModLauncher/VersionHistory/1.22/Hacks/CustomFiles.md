### General
* Added the `-noadditionalfiles` command line argument. This disables the AdditionalFiles functionality of this hack which will break mods that rely on it.
* Added the `-slowgameload` command line argument. This allows you to artificially increase load times.
* Made this hack only handle requesting a file when necessary.
* Made this hack generate a list of mods that have AdditionalFiles folders on startup and only check those mods when a file is requested instead of every mod.

### Lua Scripting
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetModTitle.md]] function.
	* This returns the current mod's title (or the title of the specified mod if one is specified).
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetModVersion.md]] function.
	* This returns the current mod's version (or the version of the specified mod if one is specified).