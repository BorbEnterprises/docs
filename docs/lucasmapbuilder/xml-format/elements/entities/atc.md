---
title: ATC
description: "This type of element is used to input and generate a new ATC chunk."
summary:
    initialVersion: "1.0"
---

# This Element {{ id this }}
This type of element is used to input and generate a new [ATC chunk](/pure3d/chunk-types/chunk-3000602.md).

These can be referenced by a [SetParameter element](../outputs/modeloutputinstructions.md#children_setparameter) inside a [ModelOutputInstructions](../outputs/modeloutputinstructions.md).

```xml
<ATC Name="NewATC">
	<!-- See Child Elements -->
</ATC>
```

* **Name**: The name of this ATC.

# Child Elements {{ id children }}
## Entries
This element inputs existing ATC entries from an [InputPure3DFile](../inputs/inputpure3dfile.md).

```xml
<InputPure3DFile Name="BaseGameATCFile" Path="$(GamePath)\art\atc\atc.p3d" />

<ATC Name="ATC">
	<Entries InputPure3DFile="BaseGameATCFile" />
</ATC>
```

* **InputPure3DFile**: The name of an [InputPure3DFile](../inputs/inputpure3dfile.md) that contains an [ATC chunk](/pure3d/chunk-types/chunk-3000602.md).
	* If the file contains multiple [ATC chunks](/pure3d/chunk-types/chunk-3000602.md) for some reason, the first one will be used.

## Entry
This element adds a new entry to the ATC file. 

These can be referenced by name with various group tags as long as this ATC is referenced in the map's [ModelOutputInstructions](../outputs/modeloutputinstructions.md).

```xml
<Entry Name="LardLadHead" SoundResouceDataName="smash" Particle="eCarExplosion" BreakableObject="" Friction="54" Mass="50" Elasticity="100" />
```

* **Name**: The name of this ATC entry to reference it by elsewhere.
* **SoundResourceDataName**: The sound resource data name for this entry.
* **Particle**: The particle effect for this entry.
* **BreakableObject**: The breakable object effect for this entry.
* **Friction**: The friction for this entry.
* **Mass**: The mass for this entry.
* **Elasticity**: The elasticity for this entry.

## OutputPure3DFile
This element specifies the [OutputPure3DFile](../outputs/outputpure3dfile.md) the new [ATC chunk](/pure3d/chunk-types/chunk-3000602.md) will go into.

```xml
<OutputPure3DFile Name="NewATCFile" Path="newatc.p3d" />

<ATC Name="NewATC">
	<!-- You should have Entries / Entry elements here to populate the new ATC chunk -->
	<!-- Otherwise, you'll just build a useless empty ATC file -->
	
	<OutputPure3DFile Name="NewATCFile" />
</ATC>
```

* **Name**: The name of the [OutputPure3DFile](../outputs/outputpure3dfile.md) this ATC should go into.

# Examples
This is an example of a new ATC file with the base game entries and a new entry. The ATC is then referenced by a [ModelOutputInstructions element](../outputs/modeloutputinstructions.md).

```xml
	<InputPure3DFile Name="BaseGameATCFile" Path="$(GamePath)\art\atc\atc.p3d"/>
	
	<OutputPure3DFile Name="NewATCFile" Path="$(OutputArtCF)\atc\atc.p3d"/>
	
	<ATC Name="NewATC">
		<Entries InputPure3DFile="BaseGameATCFile"/>
		
		<Entry Name="LardLadHead" SoundResouceDataName="smash" Particle="eCarExplosion" BreakableObject="" Friction="54" Mass="50" Elasticity="100"/>

		<OutputPure3DFile Name="NewATCFile"/>
	</ATC>

	<ModelOutputInstructions Name="Zone">
		<ExecuteInstructions Name="BaseZone"/>
		
		<SetParameter Name="VertexColours" Value="World"/>
		
		<SetParameter Name="ATC" Value="NewATC"/>
	</ModelOutputInstructions>
```

# Version History
## 1.0
Initial release.