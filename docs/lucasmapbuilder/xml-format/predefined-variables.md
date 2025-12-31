---
title: Predefined Variables
description: "This page lists all pre-defined variables that you can use in your XML files."
---

This page lists all pre-defined variables that you can use in your XML files.

These variables are case sensitive.

# MapBuilderPath
This variable contains the path to the folder the tool's executable (`LSHaRMB.exe`) is located in.

```xml
<Include Path="$(MapBuilderPath)\Rules\Zone.xml"/>
```

# GamePath
This variable contains the path that you have The Simpsons Hit & Run installed to.

```xml
<InputPure3DFile Name="L2Terra" Path="$(GamePath)\art\L2_TERRA.p3d" />
```

# ParentPath
This variable contains the path to the XML file it's being used in. This can be useful for setting path variables in your main rules file that are used by files in a sub-directory.

```xml
<SetVariable Name="LocalResourcesPath" Value="$(ParentPath)\Resources" />
```

# System Environment Variables
System environment variables can also be used like other variables in XML files.

Note that instead of the Windows syntax `%system_variable%`, you would use the same syntax as other variables in this tool: `$(system_variable)`.