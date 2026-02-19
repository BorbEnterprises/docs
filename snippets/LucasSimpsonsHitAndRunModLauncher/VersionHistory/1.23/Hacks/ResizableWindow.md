* Added the `-nomaintainwindowcentre` command line argument. This prevents this hack from trying to maintain the centre point of the game window when the game resizes it.
* Made the game terminate abruptly with no message or crash dump in the case that an exception occurs in the resizing timer callback (instead of letting Windows swallow the exception and likely cause corruption).
* Made this hack check if the game window is currently maximised instead of checking if the **Start Maximised** setting is ticked before suppressing the changing of the resolution when the game loads its settings.
* Made this hack update the game's unmaximised size and position if the game is maximised when it loads its settings.
* Made this hack force the game window to fit within the working area of the screen it's on when maintaining the window centre when the game resizes its window.
* Made this hack prevent you from resizing the client area of the game below 1 pixel on the width or height.
    Also added a `-allowzerowindowsize` command line argument to opt out of this.
* No longer resizes or repositions the window if the resolution changes when the game is in full screen.
    This became an issue with Hack Support blocking the game from resetting its Direct3D device redundantly in this version.
* No longer maintains the centre of the window when changing out of full screen.
* No longer handles resizing when the game is in full screen.