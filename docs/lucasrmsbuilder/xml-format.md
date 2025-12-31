---
title: XML Format
description: "This page documents the XML file format used to represent the data inside RMS files for this tool."
---

This page documents the XML file format used to represent the data inside RMS files for this tool.

# Composition
The **Composition** element is used as the root of the file.

It contains **FadeTransition** s, **StitchTransition** elements, **Event** elements, **State** elements, **RSDFile** elements, **Stream** elements, **Clip** elements and **Region** elements.

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<Composition SoundMemoryMax="1700000" CacheMemoryMax="2000000" StreamSizeMin="500">
	...
</Composition>
```

* **SoundMemoryMax**: Unknown.
* **CacheMemoryMax**: Unknown.
* **StreamSizeMin**: Unknown.

**Composition** attributes should only be specified on the **Composition** element if it is not the root of a file being included.

# Include
An **Include** element allows you to load another XML file containing parts of a **Composition**. This is useful for organization.

```xml
<Include Path="Transitions.xml" />
```

* **Path**: The path to the file to be included.

# FadeTransition
**FadeTransition** elements are used to define how to transition from one **Region** to another. They can also contain **Beat** elements.

```xml
<FadeTransition SourceRegion="M1_main_region" TargetRegion="M1_end_Neg_region" SourceTime="5" SourceStart="0" TargetTime="0" TargetStart="0">
	<Beat>1</Beat>
	<Beat>2</Beat>
	<Beat>3</Beat>
	<Beat>4</Beat>
</FadeTransition>
```

* **SourceRegion**: The region to handle a transition from. Use "anything" for transitioning from any region.
* **TargetRegion**: The region to handle a transition to. Use "anything" for transitioning to any region.
* **SourceTime**: Unknown.
* **SourceStart**: Unknown.
* **TargetTime**: Unknown.
* **TargetStart**: Unknown.

## Beat
```xml
<Beat>1</Beat>
```

Unknown.

# StitchTransition

Unused.

* **SourceRegion**: The region to handle a transition from. Use "anything" for transitioning from any region.
* **TargetRegion**: The region to handle a transition to. Use "anything" for transitioning to any region.
* **TransitionRegion**: Unknown. Optional.

# Event
**Event** elements are generally used by the game executable and the [StageStartMusicEvent](/hitandrun/scripting/mfk-commands/stagestartmusicevent.md) command in mission scripts to perform various event actions listed below.

```xml
<Event Name="M1_start">
	<PlayRegionAction Region="M1_main_region" RegionResumeType="Resume" />
</Event>
```

* Name: The name of the event used by the game and via mission scripts.

## PlayRegionAction
A **PlayRegionAction** element can be used to play **Region** elements.

```xml
<PlayRegionAction Region="M1_main_region" RegionResumeType="Resume" />
```

* **Region**: The name of the Region to play.
* **RegionResumeType**: Specify if the Region should Restart or Resume.

## PushRegionAction
A **PushRegionAction** element can be used to push a **Region** element to the top of the stack and play it.

```xml
<PushRegionAction Region="StoneCutters_Tunnel_region" TargetRegionResumeType="Resume" CurrentRegionResumeType="Resume" />
```
* **Region**: The name of the Region to push to the top of the stack and play.
* **TargetRegionResumeType**: Specify if the Region being pushed to the top should Restart or Resume.
* **CurrentRegionResumeType**: Specify if the Region currently playing should Restart or Resume when the Region being pushed to the top of the stack is later popped off the top of the stack.

## PopRegionAction
A **PopRegionAction** element can be used to pop a **Region** off the top of the stack.

```xml
<PopRegionAction Region="StoneCutters_Tunnel_region" />
```

* **Region**: Specify the Region to pop off the top of the stack. If the specified region is not currently on top, this action will do nothing. Optional.

## StartLayerAction
Unused.

* **LayerName**: The name of a Layer.

## StopLayerAction
Unused.

* **LayerName**: The name of a Layer.

# Event (with States)

An **Event** element with states is similar to a regular **Event** except it references a **State** element and defines multiple actions inside **StateValue** elements.

```xml
<Event Name="M2_start" State="Mission2">
	<StateValue>
		<!--Stage1-->
		<PlayRegionAction Region="M2_S1_start_region" RegionResumeType="Resume" />
	</StateValue>
	<StateValue>
		<!--Stage2-->
		<PlayRegionAction Region="M2_S2_start_region" RegionResumeType="Resume" />
	</StateValue>
</Event>
```

* **Name**: The name of the event used by the game and via mission scripts.
* **State**: The name of the state to use for this event.

## StateValue

**StateValue** elements should be defined for each state inside the referenced State. Each **StateValue** elemtn can contain the various event actions listed previously.

```xml
<StateValue>
	<!--Stage1-->
	<PlayRegionAction Region="M2_S1_start_region" RegionResumeType="Resume" />
</StateValue>
```

# State
A **State** is referenced by an **Event** that has multiple different music states that can be controlled by the [SetMusicState](/hitandrun/scripting/mfk-commands/setmusicstate.md) command in mission scripts. It can contain **Value** elements.

```xml
<State Name="Mission5">
	<Value>Stage1</Value>
	<Value>Stage2</Value>
</State>
```

* Name: The name of the state referenced by the Event and used in the first argument of SetMusicState command.

## Value
Used to define the names for the states inside a **State** to be used in the [SetMusicState](/hitandrun/scripting/mfk-commands/setmusicstate.md) command.

```xml
<Value>Stage1</Value>
```

**NOTE**: There is a limit of 6 state values among all State definitions in any given music RMS file.

# RSDFile
An **RSDFile** element defines information about an RSD File.

```xml
<RSDFile FileName="Simpsons_Theme" Size="7788348" AudioFormatEncoding="PCM" AudioFormatChannels="2" AudioFormatBitResolution="16" AudioFormatSamplingRate="24000" />
```

* **FileName**: The name of the file without the .rsd file extension. This is relative to the sound\music folder.

The following attributes should only be specified if the RSD file specified above is not present in any specified RSD Path(s):

* **Size**: The size of the file in bytes.
* **AudioFormatEncoding**: The type of encoding the file uses. Supported types are PCM, VAG, PCMB, XADP, GADP and RADP.
* **AudioFormatChannels**: The amount of audio channels the file contains.
* **AudioFormatBitResolution**: The bit resolution of the samples in the audio.
* **AudioFormatSamplingRate**: The sample rate of the audio.

# Stream
A **Stream** element represents a music track. They reference an **RSDFile** and set parameters related to it.

```xml
<Stream Name="Simpsons_Theme" RSDFile="Simpsons_Theme" TempoTrack="172 4/4" />
```

* **Name**: The name of the Stream to be referenced by Regions and Transitions
* **RSDFile**: The name of the RSDFile the Stream will use.
* **TempoTrack**: The tempo and time signature of the RSDFile.
* **TempoTrackStartBeat**: Unknown.
* **Streamed**: Unknown. Optional.

# Clip

Unused.

* **Name**: The name of the Clip.
* **RSDFile**: The name of the RSDFile the Clip will use.
* **TempoTrack** : The tempo and time signature of the RSDFile.
* **TempoTrackStartBeat**: Unknown.

# Region

A **Region** element specifies what **Stream** elements will play and how. They contain one or more **Layer** elements.

```xml
<Region Name="FE_region">
	<Layer Name="l">
		<LogicRepeatEvent>
			<StreamEvent Name="Simpsons_Theme" />
		</LogicRepeatEvent>
	</Layer>
</Region>
```

* **Name**: The name of the Region.
* **ExitRegion**: The name of a Region to switch to when this region ends. Optional.
* **Volume**: The volume of the region's contents. Optional, defaults to 1.0.

## Layer
A **Layer** element can contain various types of sequence event listed below.

```xml
<Layer Name="l">
	<LogicOrEvent>
		<StreamEvent Name="Sunday_Drive_End_Sus1" />
		<StreamEvent Name="Sunday_Drive_End_Sus3" />
	</LogicOrEvent>
</Layer>
```

* **Name**: The name of the layer.
* **Constant**: Unknown. Optional, defaults to true.
* **Volume**: Specify the volume of the layers contents. Optional, defaults to 1.0.

### LogicAndEvent
A **LogicAndEvent** simply executes every sequence event inside it.

```xml
<LogicAndEvent>
	<LogicRepeatEvent Times="2">
		...
	</LogicRepeatEvent>
	<LogicOrEvent>
		...
	</LogicOrEvent>
</LogicAndEvent>
```

### LogicRepeatEvent
A **LogicRepeatEvent** will repeat the sequence events inside it forever or for the specified number of times.

```xml
<LogicRepeatEvent MinTimes="2" MaxTimes="3">
	<LogicAndEvent>
		<SilenceEvent Time="2000" />
		<SilenceEvent Time="3000" />
	</LogicAndEvent>
</LogicRepeatEvent>
```

* **Times**: Specify the amount of times to repeat the event.

OR

* **MinTimes**: Specify the minimum amount of times to repeat the event.
* **MaxTimes**: Specify the maximum amount of times to repeat the event.

OR

Specify no attributes to loop the sequence of events indefinitely.

### LogicOrEvent
A **LogicOrEvent** will execute one of the sequence events inside it at random.

```xml
<LogicOrEvent>
	<StreamEvent Name="Tuba_001" />
	<StreamEvent Name="Tuba_002" />
	<StreamEvent Name="Tuba_003" />
	...
	<StreamEvent Name="Tuba_065" />
	<StreamEvent Name="Tuba_068" />
	<StreamEvent Name="Tuba_069" />
</LogicOrEvent>
```

### SilenceEvent
A **SilenceEvent** will play silence for the specified amount of time.

```xml
<SilenceEvent Time="2000" />
<SilenceEvent MinTime="2000" Maxtime="3000" />
```

* **Time**: Specify the amount of time.

OR

* **MinTime**: Specify the minimum amount of time.
* **MaxTime**: Specify the maximum amount of time.

### StreamEvent
A **StreamEvent** will play the specified Stream.

```xml
<StreamEvent Name="Simpsons_Theme" />
```

* **Name**: The name of the Stream to play.

### ClipEvent
Unused.

* **Name**: The name of the Clip to play.

### VarVolumeEvent
Unused.

* **Volume**: Unknown.

### VarPitchEvent
Unused.

* **Pitch**: Unknown.

### VarVolumeRandMinEvent
Unused.

* **VolumeRandMin**: Unknown.

### VarVolumeRandMaxEvent
Unused.

* **VolumeRandMax**: Unknown.

### VarPitchRandMinEvent
Unused.

* **PitchRandMin**: Unknown.

### VarPitchRandMaxEvent
Unused.

* **PitchRandMax**: Unknown.

### VarAuxGainEvent
Unused.

* **AuxNumber**: Unknown.

AuxGain: Unknown.

### VarPositionalEvent
Unused.

* **Positional**: Unknown.

### VarPosFallOffEvent
Unused.

* **PosFallOff**: Unknown.

### VarPosDistMinEvent
Unused.

* **PosDistMin**: Unknown.

### VarPosDistMaxEvent
Unused.

* **PosDistMax**: Unknown.

### CallbackEvent
Unused.

* **CallbackName**: Unknown.

### Beat
Unknown.

```xml
<Beat>1</Beat>
```

# Notes
The names of elements and attributes in this XML format are derived from Radical's official names as the RMS format stores all of the RadMusic class and field names within it.

Some other design decisions were derived from the plain text RMS format used in other Radical games such as *The Incredible Hulk: Ultimate Destruction*.

Items in this documentation that say "Unknown." are used in Hit & Run but their functionality is not understood.

Items in this documentation that say "Unused." are not used in Hit & Run and their functionality is not understood.