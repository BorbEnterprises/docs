* Added support for setting a visual steering multiplier for car wheels.
	* You can set one for the front wheels via the `FrontSteeringVisualMultiplier` property and one for the back wheels via the `RearSteeringVisualMultiplier`.
	* You can also set one for an individual wheel via the `Wheel?SteeringVisualMultiplier`, substituting the `?` for the wheel index:
		* 0 for the back right wheel.
		* 1 for the back left wheel.
		* 2 for the front left wheel.
		* 3 for the front right wheel.
		* Unless, of course, you're Radical and you're making the Family Sedan (`famil_v`) wherein 2 and 3 are inexplicably swapped around.
* Added support for additional Fake Wheels on cars via the new `[FakeWheel]` section.
	* Fake Wheels have various configuration options and work by copying and/or multiplying values of any of the car's four real wheels.
* Added support for new `[Car]` sections as an alternative to using the car's name as the name of the section.
	* These sections use the new `Name` property instead to identify the car.
* Added support for setting skid mark width multipliers for each of the car's real wheels.
	* You can set one for the front wheels via the `FrontSkidMarkWidthMultiplier` property and one for the back wheels via the `RearSkidMarkWidthMultiplier`.
	* You can also set one for an individual wheel via the `Wheel?SkidMarkWidthMultiplier`, substituting the `?` for the wheel index.