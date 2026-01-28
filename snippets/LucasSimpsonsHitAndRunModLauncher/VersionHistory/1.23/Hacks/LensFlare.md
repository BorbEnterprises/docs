* Added a description to this hack.
* Made this hack work differently (using an [occlusion query](https://docs.microsoft.com/en-us/windows/win32/direct3d9/queries) instead of a lockable render target) when using [[/LucasSimpsonsHitAndRunModLauncher/Hacks/Direct3D9.md]].
	* Also added a `-noocclusion` command line argument to opt out of this.
	* Also added a `-occlusionsleep` command line argument.