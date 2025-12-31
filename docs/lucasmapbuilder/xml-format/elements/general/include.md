---
title: Include
description: "This type of element allows you to load another XML file containing more rules. This is useful for organization and sharing XML files between multiple map projects."
summary:
    initialVersion: "1.0"
---

# This Element
This type of element allows you to load another XML file containing more rules. This is useful for organization and sharing XML files between multiple map projects.

```xml
<!-- Include base zone rules -->
<Include Path="$(ModelBuilderPath)\Rules\Zone.xml"/>
```

* **Path**: The path to the file to be included.
* **Sandbox**: TODO.
    * Defaults to false.
    * Forced to true if the file being included has `Once` set to `true` on it's [Build XML Element](build.md).
* **Firewall**: TODO.
    * Defaults to false.
* **NoOutput**: TODO.
    * Defaults to false.

# Child Elements
This type of element has no children.

# Version History
## 1.0
Initial release.