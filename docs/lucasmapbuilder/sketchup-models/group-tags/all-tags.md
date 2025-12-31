---
title: All Group Tags
description: "This page documents the various \"group tags\" that Input SketchUp models can utilize in their group names to invoke special rules and build processes for the group's contents."
---

This page doucments the various "group tags" that Input SketchUp models can utilize in their group names to invoke special rules and build processes for the group's contents.

These tags are defined by the included XML files in the "Rules" folder next to the tool's executable. 

Each page lists which files can be included with an [Include](../../xml-format/elements/all-elements.md#include) element in your rules XML to use the tag.

# General Tags
These are general use group tags.

{{ summary lucasmapbuilder/sketchup-models/group-tags/general/excludefrombounds | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/general/flipfaces | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/general/transform | 2 | Learn more... }}

# Billboard Tags
These tags are used to create billboards.

{{ summary lucasmapbuilder/sketchup-models/group-tags/billboards/billboardquadgroup | 2 | Learn more... }}

# Camera Tags
These tags are used to create cameras.

{{ summary lucasmapbuilder/sketchup-models/group-tags/cameras/animatedcamera | 2 | Learn more... }}

# Collision Tags
These tags are used to create and configure collision.

{{ summary lucasmapbuilder/sketchup-models/group-tags/collision/fence | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/collision/intersect | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/collision/nocollision | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/collision/staticphys | 2 | Learn more... }}

## Collision Components
These tags are used specifically on [CollisionBox Components](../special-components.md#collisionbox), a [CollisionCylinder Components](../special-components.md#collisioncylinder) and [CollisionSphere Components](../special-components.md#collisionsphere).

{{ summary lucasmapbuilder/sketchup-models/group-tags/collision/components/density | 3 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/collision/components/flatend | 3 | Learn more... }}

# Entity Tags
These tags are used to create props and other instantiable objects.

{{ summary lucasmapbuilder/sketchup-models/group-tags/entities/animdynaphys | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/entities/animobj | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/entities/dynaphys | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/entities/inststatentity | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/entities/inststatphys | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/entities/nonworldmesh | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/entities/staticentity | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/entities/staticentitygroup | 2 | Learn more... }}

# HUD Map Tags
These tags are used to control what meshes are part of the HUD map and what color they are, as well as which HUD map they're apart of.

{{ summary lucasmapbuilder/sketchup-models/group-tags/hudmaps/building | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/hudmaps/hudmap | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/hudmaps/nonhudmapmesh | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/hudmaps/road | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/hudmaps/sidewalk | 2 | Learn more... }}

# Lighting Tags
These tags are used to apply lighting to groups.

{{ summary lucasmapbuilder/sketchup-models/group-tags/lighting/vertexcolours | 2 | Learn more... }}

# Locator Tags
These tags are used to create various types of [Locators](../../../pure3d/chunk-types/chunk-3000005.md).

{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/carstart | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/coin | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/collectorcard | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/deathzone | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/event | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/interiorentry | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/interiorentrystartend | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/interiorexit | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/jumpzone | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/loadzone | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/pedgroup | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/purchaseskin | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/spring | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/staticcam | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/summonvehiclephone | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/teleport | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/waypoint | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/locators/wrench | 2 | Learn more... }}

# Path Tags
These tags are used to create [Paths](../../../pure3d/chunk-types/chunk-300000B.md).

{{ summary lucasmapbuilder/sketchup-models/group-tags/paths/path | 2 | Learn more... }}

# Road Tags
These tags are used to create [Intersections](../../../pure3d/chunk-types/chunk-3000004.md) and [Roads](../../../pure3d/chunk-types/chunk-3000003.md).

{{ summary lucasmapbuilder/sketchup-models/group-tags/roads/intersection | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/roads/road | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/roads/roadpair | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/roads/simpleroad | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/roads/simpleroadpair | 2 | Learn more... }}

# World Sphere Tags
These tags are used to create [World Spheres](../../../pure3d/chunk-types/chunk-3F0000B.md).

{{ summary lucasmapbuilder/sketchup-models/group-tags/world-spheres/animworldsphere | 2 | Learn more... }}
{{ summary lucasmapbuilder/sketchup-models/group-tags/world-spheres/worldsphere | 2 | Learn more... }}