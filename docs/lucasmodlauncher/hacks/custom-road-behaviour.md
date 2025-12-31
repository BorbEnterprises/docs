---
title: Custom Road Behaviour
description: "This hack allows mods to define custom behaviour for specific roads."
---

**This hack must be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

This hack allows mods to define custom behaviour for specific roads.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=CustomRoadBehaviour
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `CustomRoadBehaviour.xml` and add the parameters necessary for your mod inside it.

```xml
<?xml version="1.0" encoding="utf-8"?>
<CustomRoadBehaviour>
	<!--
		
	<Behaviour>
		Name: The name of the behaviour.
			UTurnTolerance
			DisableTrafficGroundSnapping
		Value: The value to give the behaviour.
	
	<Level>
		Index: The index of the level (zero-based).
		OR
		Number: The number of the level (one-based).
	
		<Road>
			Name: The name of the road.
	
	-->

	<Level Number="1">
		<Behaviour Name="UTurnTolerance" Value="0.10" />
		
		<!-- Bridge Roads by the School in Road Rage Returns -->
		<Road Name="R031">
			<Behaviour Name="DisableTrafficGroundSnapping" Value="true" />
		</Road>
		<Road Name="R032">
			<Behaviour Name="DisableTrafficGroundSnapping" Value="true" />
		</Road>
	</Level>
</CustomRoadBehaviour>
```

# Version History
## 1.22
Added support for a `Number` attribute on `<Level>` elements.

## 1.16
Added this hack.