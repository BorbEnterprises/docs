---
title: Joint
description: This tag is used to assign the contents of a group to a joint in various types of complex entities.
status:
    class: "wip"
summary:
    initialVersion: "1.0"
---

This tag is used to assign the contents of a group to a joint in various types of complex entities.

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `Drawables.xml`
* `Zone.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

TODO

# Syntax
```text
<JointName> [Joint]
```

* **Name**: The name of the joint to attach this group to.

# Group Structure
TODO

# Examples
TODO

# Other Tags
These are other tags that can be used with this tag to configure it further.

## Effect
TODO

```text
<JointName> [Joint] [Effect] [<EffectName>]
```

## Group
TODO

```text
<JointName> [Joint] [Group] [<AnimationGroupName>]
```

# Version History
## 1.0
Initial release.