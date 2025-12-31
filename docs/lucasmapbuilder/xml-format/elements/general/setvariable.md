---
title: SetVariable
description: "This type of element allows you to set variables that can be referenced elsewhere."
summary:
    initialVersion: "1.0"

# TODO: Update the fuck out of the first note to account for Local variables and Sandboxed/Firewalled XML files.
---

# This Element
This type of element allows you to set variables that can be referenced elsewhere.

```xml
<SetVariable Name="LocalResourcesPath" Value="$(ParentPath)\Resources" />
```

* **Name**: The name of the variable.
    * Note that 
* **Value**: The value of the variable.
* **Local**: Sets if the variable is local to the file using it.
    * Defaults to false.

## Notes

* Variables can be used anywhere after they are defined including inside other variable definitions as showcased above. 
* There are [predefined variables](../../predefined-variables.md) that are available by default.
    * These are prioritised below variables set in XML files.


# Child Elements
This type of element has no children.

# Version History
## 1.0
Initial release.