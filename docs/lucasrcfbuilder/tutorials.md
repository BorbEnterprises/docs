---
title: Tutorials
description: "This page contains a few short tutorials on how to use the RCF Builder."
---

This page contains a few short tutorials on how to use the RCF Builder.

These instructions can be used in a Command Prompt window or in a batch file. You will need to replace the paths in these examples with where you put the tool and where you have your input/output files and folders.

**This tool currently only supports version 1.2 of the RCF format, the version used by The Simpsons Road Rage and The Simpsons Hit & Run.**

# Extracting an RCF
To extract an RCF file, use the following command line arguments:

```text
"C:\path\to\LRCFB.exe" -inputrcf "C:\path\to\input\file.rcf" -outputdir "C:\path\to\extract\to"
```

# Building an RCF
## From scratch
To build an RCF file from scratch, use the following command line arguments:

```text
"C:\path\to\LRCFB.exe" -inputdir "C:\path\to\input\from" -outputrcf "C:\path\to\build\to\file.rcf"
```
You must also use `-bigendian` when building files for Nintendo GameCube games.

## From an existing RCF and a directory
To build an RCF file from an existing RCF and a directory, use the following command line arguments:

```text
"C:\path\to\LRCFB.exe" -inputrcf "C:\path\to\input\from\file.rcf" -inputdir "C:\path\to\input\from\dir" -outputrcf "C:\path\to\build\to\file.rcf"
```

For files that exist in both the RCF and the directory, the latter will be prioritized.

You must also use `-bigendian` when building files for Nintendo GameCube games.

## Updating an RCF
To update the contents of an RCF file with that of a directory, use the following command line arguments:

```text
"C:\path\to\LRCFB.exe" -rcf "C:\path\to\input\from\file.rcf" -inputdir "C:\path\to\input\from"
```
   
You must also use `-bigendian` when building files for Nintendo GameCube games.