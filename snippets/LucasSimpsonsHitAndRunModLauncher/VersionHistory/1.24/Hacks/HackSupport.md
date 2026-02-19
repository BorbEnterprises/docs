* Improved handling of saved games with purchased cars and/or skins at indices that are not bound in the current rewards file with [a very informative message](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/InvalidSaveFileMessage.png).
* Made the "hack events" Debug Text page (available when using the -testing command line argument) [show the top 18 internal hack events](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/InternalHackEvents.png) in addition to the information it already showed.
* Changed part of the error message shown when no audio device is connected from "Please connect an audio output device or install a virtual audio device (such as VB-Audio Virtual Cable) and launch the game again." to "You can enable the No Audio mod hack to allow the game to run without an audio output device or connect one and launch the game again.".
* Made it so Buffer overruns (and possibly other error messages from the game's instance of the Microsoft Visual C++ Runtime) save crash dumps.
	* These types of crash also now have [more modern looking dialogs](/img/LucasSimpsonsHitAndRunModLauncher/Hacks/HackSupport/BufferOverrun.png).
	* Due to the nature of buffer overrun detection (including the fact that it is detection for corruption that has already occured but shouldn't have had a chance to do anything dangerous (in terms of security, not stability)), it may not always be feasible to get much information from these crash dumps.
	* Also added the `-nohandlecrtmessagebox` command line argument to opt out of this.
* Made creating an additional swap chain (when the Resizable Window mod hack is enabled and not using the `-noadditionalswapchain` command line argument or when using the `-additionalswapchain` command line argument) terminate the game if the device window handle ([hDeviceWindow](https://docs.microsoft.com/en-us/previous-versions/ms886318%28v%3dmsdn.10%29)) is invalid according to [IsWindow](https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-iswindow).
	* This is done after an assert when using the `-testing` command line argument.
	* This is to prevent asserts when closing the game window before the game loads simpsons.ini.
* Made CreateAdditionalSwapChain failing when creating an additional swap chain only assert when using the `-testing` command line argument.
* Made failing to create an additional swap chain fall back to not using an additional swap chain.
	* This also disables further attempts to use an additional swap chain.
	* This is the same behaviour as using the `-noadditionalswapchain` argument.