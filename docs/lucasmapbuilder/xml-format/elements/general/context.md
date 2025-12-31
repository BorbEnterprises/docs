---
title: Context
description: "This type of element allows you to scope other elements inside it. This is like using the Include XML Element without actually including another file."
summary:
    initialVersion: "1.0"
---

# This Element
This type of element allows you to scope other elements inside it. This is like using [Include XML Element](include.md) without actually including another file, as a result it is also similar to a [Build XML Element](build.md) in concept.

```xml
<!-- Sandbox stuff inside this element -->
<Context Sandbox="true">
    <!-- This variable can only be used inside this context -->
    <SetVariable Name="Example" Value="Potato">
</Context>
```

* **Sandbox**: TODO.
    * Defaults to false.
    * Forced to true if the file being included has `Once` set to `true` on it's [Build XML Element](build.md).
* **Firewall**: TODO.
    * Defaults to false.
* **NoOutput**: TODO.
    * Defaults to false.

# Child Elements
All elements except for [`Build`](build.md) elements can be nested inside these elements.

# Version History
## 1.0
Initial release.