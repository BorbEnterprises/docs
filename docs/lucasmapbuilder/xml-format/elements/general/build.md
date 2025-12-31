---
title: Build
description: "This type of element is used as the root of each XML file."
summary:
    initialVersion: "1.0"
---

# This Element
This type of element is used as the root of each XML file.

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<Build Once="false">
    <!-- All other elements go in here -->
</Build>
```

* **Once**: Whether or not this XML file should only get included one time.
    * Defaults to false.

# Child Elements
All other elements either go either directly or indirectly inside this element.

# Version History
## 1.0
Initial release.