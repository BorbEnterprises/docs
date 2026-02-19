Added a new **Method** setting for controlling how the frame limiting is done:
* **Waitable Timer**: The original method that's consistent but slightly inaccurate. This is still the default setting.
* **Sleep**: A different method that may work better but also may cause stuttering on some computers.
* **Busy Wait**: An extremely intensive but effective method.
* **Sleep and Busy Wait**: A combination of the previous 2 that sleeps for most of a frame and then busy waits for the rest.