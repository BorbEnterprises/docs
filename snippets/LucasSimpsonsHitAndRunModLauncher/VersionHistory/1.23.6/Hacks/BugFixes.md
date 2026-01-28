Added **Vehicles > Phone Booth Camera Pan Active Camera Change**.

This fixes a bug related to pressing the in-car change camera button during the phonebooth's camera pan. Without this bug fix, doing so will cancel the camera and switch your camera to the mouse controlled camera until the game changes your camera again (such as when getting in a car). If you use mission select to select a mission without getting in a car, you will be able to skip the next mission start camera.

We also added a `FixRelativeAnimatedCamCameraChange` property to the `[Camera]` section of `BugFixes.ini` to opt in to this.

This bug fix exists as a result of research done by aldelaro5.