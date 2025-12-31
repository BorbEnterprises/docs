---
title: MaterialRules
description: "This type of element allows you to define rules for handling materials on an InputSketchUpModel."
summary:
    initialVersion: "1.0"
---

# This Element {{ id this }}
This type of element allows you to define rules for handling materials on an [InputSketchUpModel](../inputs/inputsketchupmodel.md).

```xml
<MaterialRules Name="World">
	<!-- Selector elements go here -->
</MaterialRules>
```

* **Name**: The name of these rules to be referenced by other elements.

# Child Elements {{ id children }}
## Selector
This type of element is used directly inside [MaterialRules](#this) elements to select a material by name using regex patterns.

```xml
<MaterialRules Name="World">
    <!-- Select the materials named "prop_phonebooth_smoke" or "prop_shadow" -->
    <Selector Pattern="^(?:prop_phonebooth_smoke|prop_shadow)$" Exclusive="true">
        <!-- Parameter elements go here -->
    </Selector>
</MaterialRules>
```

* **Pattern**: The regex pattern to use to match the name of the material / group.
* **Exclusive**: Exclusively apply the rules in this Selector once the group is matched.
* **ForceOverride**: Force the rules in this Selector to be applied regardless of exclusivity.

## Parameter
These elements are used inside [Selector](#selector) elements to set parameters for a specific material or materials.

```xml
<MaterialRules Name="World">
    <Selector Pattern="^(?:prop_phonebooth_smoke|prop_shadow)$" Exclusive="true">
        <!-- Set the blend mode of the selected materials to Subtractive -->
        <Parameter Name="BlendMode" Value="Subtractive"/>
    </Selector>
</MaterialRules>
```

* **Name**: The name of the parameter. 
    * **AlphaTest**: Set whether or not the material uses alpha test.
        * Defaults to false.
    * **Animation**: Set the name of a [TextureAnimation](../animations/textureanimation.md) to use on this material.
    * **BlendMode**: Set the blend mode of the material.
        * `None`
            * Default.
        * `Alpha`
        * `Additive`
        * `Subtractive`
    * **EnvironmentMapTextureName**: Set the environment map Texture name.
        * Defaults to no enviroment map.
    * **EnvironmentMapRed**: Set the red color value of the environment map. 
        * Defaults to 255.
    * **EnvironmentMapGreen**: Set the green color value of the environment map. 
        * Defaults to 255.
    * **EnvironmentMapBlue**: Set the blue color value of the environment map. 
        * Defaults to 255.
    * **Lighting**: Set whether or not the material will have dynamic lighting.
        * Defaults to false.
    * **Name**: Set the name of the material.
        * Defaults to the name specified in SketchUp.
    * **Opacity**: Sets the opacity of every vertex in every face this material is used on.
        * From 0 to 1.
        * Defaults to 1 (effectively).
    * **Set**: Replace this material's texture with a [Set](../../../../pure3d/chunk-types/chunk-3000110.md).
    * **TexturePath**: Set the path to a texture to replace this material's texture with.
    * **TwoSided**: Set whether or not the material is two-sided.
    * **UVMode**: Set the UV mode of the material.
        * `Tile`
            * Default.
        * `Clamp`
* **Value**: The value of the parameter.

# Notes

* When building P3D files, Materials ultimately become Shaders. Many of the parameters set here directly correspond to ones that can be found in P3D files.
* These parameters can use values selected inside the regex given to the the parent `Selector` element.

# Version History
## 1.0
Initial release.