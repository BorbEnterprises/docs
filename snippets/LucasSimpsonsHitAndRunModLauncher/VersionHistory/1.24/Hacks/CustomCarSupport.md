* Added the `NoBumperCam` property.
	* This just disables the bumper cam for a given car, like how the RC Car does by default.
* Made it so this hack only patches the game code for the specific functionality being used by the currently loaded mods.
* Added the `Husk` property.
	* This specifies what car should be used as this vehicle's husk when it explodes.
	* The vehicle used for this property should be marked as a husk using the `IsHusk` property below.
* Added the `IsHusk` property.
	* This marks a car as being a husk, giving it certain special properties that the charred husk has by default.
* Added the `BackWheelSparks` property.
	* This makes a vehicle's back wheels emit sparks like how the charred husk does by default.
* Added the `Invincible` property.
	* This makes it impossible to destroy the vehicle.