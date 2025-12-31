---
title: Override Shader Parameters
description: This hack allows mods to override shader parameter values globally or for specific shaders.
---

**This hack must be [required by a mod](all-hacks.md#mod-requirable-hacks) to be enabled.**

This hack allows mods to override shader parameter values globally or for specific shaders.

# Requiring This Hack
To require this hack, add this line to your mod's Meta.ini:

```ini
RequiredHack=OverrideShaderParameters
```

Your mod must provide a configuration file when requiring this hack.

# Configuring This Hack
To configure this hack, create a file named `OverrideShaderParameters.xml` and add the parameters necessary for your mod inside it.

```xml
<?xml version="1.0" encoding="utf-8"?>
<OverrideShaderParameters>
	<!--
	
	Override Shader Parameters
		Override shader parameters globally or for specific shaders.

	<Shader>
		<Parameter>
			Name: The name of the parameter type you want to override. Optional, not specifying a name will apply the overrides to every shader.
				This name can use * and ? wildcards. * matches any amount of characters, ? matches a specific amount.
			Value: The value of the parameter. Optional, not specifying this will indicate to use the value in P3D files.
				For simplicity, "false" and "true" can be used in place of 0 and 1 respectively for Shader Integer Parameters.
				
				[Shader Colour Parameters can specify each channel seperately as well]
			Red: The parameters red value.
			Green: The parameters green value.
			Blue: The parameters blue value.
			Alpha: The parameters alpha value. Optional.
		
	-->
	
	<Shader>
		<!-- No value specified so use whatever the shaders say instead of forcing it -->
		<Parameter Name="2SID" />
	</Shader>
	
	<Shader Name="shadername1">
		<!-- Force 2SID off regardless of what the shader specifies -->
		<Parameter Name="2SID" Value="false"/>
	</Shader>
	
	<Shader Name="shadername2">
		<!-- Force 2SID on regardless of what the shader specifies -->
		<Parameter Name="2SID" Value="true"/>
	</Shader>
	
	<Shader Name="famil_v*">
		<!-- Apply a red diffuse color to most of the shaders of the Family Sedan -->
		<Parameter Name="DIFF" Value="0xFFFF0000" />
	</Shader>
	
	<Shader Name="marge_v*">
		<!-- Apply a blue diffuse color to most of the shaders of the Canyonero -->
		<Parameter Name="DIFF" Red="0" Green="0" Blue="255" Alpha="255" />
	</Shader>
</OverrideShaderParameters>
```

<!-- TODO: Example of ROTV vector Parameter (X, Y, Z values) -->
<!-- Example that doesn't make sense to provide: -->
<!-- 0.000628961774 -->
<!-- 0.000000000 -->
<!-- -6.12717438 -->

# Version History
## 1.23.4

* Added support for Vector parameters.
* Added support for the `ROTV`, `REFI`, `REFB` and `REFC` parameters.

## 1.20.2
Fixed an issue where "2SID" was being disabled on certain shaders the game dynamically created causing certain things to appear invisible such as smoke from damaged vehicles and the coin sparkle.

## 1.20.1
Added this hack.