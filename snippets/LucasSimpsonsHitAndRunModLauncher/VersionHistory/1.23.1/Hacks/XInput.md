* Added a **Button Names** setting.
* Added a **Default Controls** setting.
* Added two new settings to allow you to use both triggers simultaneously and multiple D-pad buttons simultaneously. These are both enabled by default.
* Added a `-noxinput` command line argument. This makes it so the hack does not make the game use XInput.
    * Despite this seeming counter-intuitive, it would still allow the other features of the hack to work while Windows' XInput-to-DirectInput backwards compatibility handles inputs.
* Added a `-noxinputdisable` command line argument. This makes it so XInput does not get disabled when the window is defocused.
* Fixed an inconsistency with the function used when [XInputEnable](https://docs.microsoft.com/en-au/windows/desktop/api/xinput/nf-xinput-xinputenable) is not available or when using the `-noxinputenable` command line argument.
* Fixed an issue where the Y (vertical) axis of the right stick was inverted.
    * This fix will require you to manually fix your control bindings.