* Added support for hardware skinning.
	* This can still be opted out of with the `-nohardwareskinning` command line argument.
	* The hack falls back to not using hardware skinning for Primitive Groups with shaders with a PDDI Shader other than "simple" or "error" for compatibility with mods that for some reason relied on Direct3D 9 to allow environment maps to work on Skins.
	* Mods with Skins that have Primitive Groups that are missing skinning information would crash without hardware skinning.