---
title: ModelOutputInstructions
description: This type of element is used to define instructions on how to build output files.
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

# This Element
This type of element is used to define instructions on how to build output files.

```xml
<ModelOutputInstructions Name="Main">
    <!-- See Child Elements -->
</ModelOutputInstructions>
```

* **Name**: The name of these instructions to be referenced by other elements.

# Child: AddSelector
This type of element is used inside [ModelOutputInstructions](#this-element) elements to select something by name using regex patterns.

```xml
<ModelOutputInstructions Name="Main">
    <!-- Select the group named "Terra" specifically -->
    <AddSelector Pattern="^Terra$" Exclusive="true">
        <!-- Instuctions here -->
    </AddSelector>

    <!-- Select any group that starts with Zone0 followed by a number -->
    <AddSelector Pattern="^Zone0*(\d+)$" Exclusive="true">
        <!-- Instuctions here -->
    </AddSelector>
</ModelOutputInstructions>
```

* **Pattern**: The regex pattern to use to match the name of the material / group.
* **Exclusive**: Exclusively apply the rules in this Selector once the group is matched.
* **ForceOverride**: Force the rules in this Selector to be applied regardless of exclusivity.

# Child: ExecuteInstructions
TODO

# Child: AddOutputZone
TODO

# Child: RemoveOutputZone
TODO

# Child: ClearOutputZones
TODO

# Child: AddOutputPure3DFile
TODO

# Child: RemoveOutputPure3DFile
TODO

# Child: ClearOutputPure3DFiles
TODO

# Child: SetParameter
TODO

# Child: UnsetSelector
TODO

# Child: AddEffect
TODO

# Child: Warning
TODO

# Version History
## 1.0
Initial release.