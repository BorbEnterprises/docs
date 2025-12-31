---
title: Command Line Arguments
description: "This page lists all of the command line arguments for the map builder."
---

This page lists all of the command line arguments for the map builder.

# Rules XML Path
Passing a path to a Rules XML file tells the map builder to execute the rules inside it.

```text
@"C:\path\to\LSHaRMB.exe" "Build.xml"
```

# -log
Enables logging to the log file. 

Enabled by default unless `-nooutput` is enabled.

```text
@"C:\path\to\LSHaRMB.exe" "Build.xml" -nooutput -log
```

# -nolog
Disables logging to the log file. 

Enabled by default if `-nooutput` is enabled.

```text
@"C:\path\to\LSHaRMB.exe" "Build.xml" -nolog
```

# -nooutput
Prevents the Map Builder from actually building any output files.

```text
@"C:\path\to\LSHaRMB.exe" "Build.xml" -nooutput
```

# -nopause
Suppresses the `Press any key to continue . . .` prompt at the end of the building process.

This can be useful for building multiple maps in rapid succession.

```text
@"C:\path\to\LSHaRMB.exe" "Build1.xml" -nopause
@"C:\path\to\LSHaRMB.exe" "Build2.xml"
```

# -sketchup16
Forces the Map Builder to use the SketchUp 2016 API.

```text
@"C:\path\to\LSHaRMB.exe" "Build.xml" -sketchup16
```

# -sketchup17
Forces the Map Builder to use the SketchUp 2017 API. 

Enabled by default if you're using Windows Vista or newer.

```text
@"C:\path\to\LSHaRMB.exe" "Build.xml" -sketchup17
```