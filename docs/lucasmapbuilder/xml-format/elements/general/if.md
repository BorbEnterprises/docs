---
title: If
description: "This type of element allows you to only use certain rules if the specified conditions are met. This is useful for doing checks in shared XML files."
summary:
    initialVersion: "1.0"
---

# This Element
This type of element allows you to only use certain rules if the specified conditions are met. This is useful for doing checks in shared XML files.

```xml
<If Type="Number" Value1="$(Level)" Operator="EqualTo" Value2="1">
    <!-- Only execute the rules in this block if the "Level" variable is set to 1 -->
</If>
```

* **Type**: The type of the two values you're comparing.
    * **Boolean**: The two values must be booleans (`true`/`1` or `false`/`0`).
    * **Number**: The two values will be treated as numbers. For example, `1.0` would be equal to `1`.
    * **String**: The two values will be treated as strings. For example, `1.0` is not equal to `1`.
* **Value1**: The first value to compare.
* **Operator**: The operator with which to compare Value1 and Value2. <!-- TODO: Get a list of supported operators from Lucas -->
    * **EqualTo**: True when the two values are equal.
    * **NotEqualTo**: True when the two values are *not* equal.
    * **GreaterThan**: True when Value1 is greater than Value2. 
        * Using this operator will force the `Type` to be `Number`.
    * **LessThan**: True when Value1 is less than Value2.
        * Using this operator will force the `Type` to be `Number`.
    * **GreaterThanOrEqualTo**: True when Value1 is greater than or equal to Value2.
        * Using this operator will force the `Type` to be `Number`.
    * **LessThanOrEqualTo**: True when Value1 is less than or equal to Value2.
        * Using this operator will force the `Type` to be `Number`.
* **Value2**: The second value to compare.

# Child Elements
All elements valid at the location of the `If` elements can be nested inside these elements.

# Notes
This element can be inside all other elements.

# Version History
## 1.0
Initial release.