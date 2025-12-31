---
title: AnimatedCamera
description: "This tag is used to create an animated camera such as those used when starting a mission."
summary:
    initialVersion: "1.0"
---

This tag is used to create an animated camera such as those used when starting a mission. 

# Usage
{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-include }}

* `AnimatedCameras.xml`
* `Drawables.xml`

{{ snippet lucasmapbuilder/sketchup-models/group-tags/usage-execute }}

* `AnimatedCameras`
    * Recommended.
* `Branch`
    * Only when including `Drawables.xml`.
* `SceneGraph2`
    * Only when including `Drawables.xml`.

# Syntax
```text
<CameraName> [AnimatedCamera] [<Length>]
```

* **CameraName**: The name of the camera used to reference it in script commands.
* **Length**: The amount of time the camera animation will last in seconds.

# Group Structure
This tag requires certain other groups with special names and tags inside the group its applied to:

* A group named `Path` containing a single connected series of lines that represent the path of the camera.
* Two or more [Camera components](../../special-components#camera) inside that group.
    * One camera should be named `Start` and one should be named `End`.
        * These should be placed at opposite ends of the `Path`.
    * Additional unnamed `Camera` components can be used to fine tune the camera's position as it moves along the `Path`.

# Examples
This is an example of a group with this tag applied to it:

![animated camera hierarchy](/img/lucasmapbuilder/sketchup-models/group-structures/animated-camera/hierarchy.png)

This is an example of the contents of that group in SketchUp's 3D view:

![animated camera 3d view](/img/lucasmapbuilder/sketchup-models/group-structures/animated-camera/3d-view.png)

# Other Tags
These are other tags that can be used with this tag to configure it further.

## OrientToPath
This tag can be used to make the camera orient itself to the `Path`.

```text
<CameraName> [AnimatedCamera] [<Length>] [OrientToPath]
```

# Version History
## 1.0
Initial release.