---
title: Command Line Arguments
description: "This page lists the command line arguments for the tool."
---

These are the various command line arguments that the RCF Builder supports.

# -inputrcf

**Added in version 1.0.**

Specify an input RCF file to output.

```text
-inputrcf "C:\path\to\file.rcf"
```

# -inputdir

**Added in version 1.0.**

Specify an input directory to output.

```text
-inputdir "C:\path\to\folder"
```

# -outputrcf

**Added in version 1.0.**

Specify an output RCF to build any inputs to.

```text
-outputrcf "C:\path\to\file.rcf"
```

# -outputdir

**Added in version 1.0.**

Specify an output directory to extract any inputs to.

```text
-outputdir "C:\path\to\folder"
```

# -rcf

**Added in version 1.0.**

Specify an RCF file to update with inputs.

This preserves the times of input and enables `-memory`.

```text
-rcf "C:\path\to\file.rcf"
```

# -bigendian

**Added in version 1.0.**

Builds a big endian RCF file for GameCube games. The tool defaults to little endian.

```text
-bigendian
```

# -alignment

**Added in version 1.0.**

Pads each file to the specified amount. Defaults to 2048, use 0 for no alignment.

```text
-alignment "2048"
```

# -preservedirtimes

**Added in version 1.0.**

Keep any modified dates when building an RCF file.

```text
-preservedirtimes
```

# -preservercftimes

**Added in version 1.0.**

Keep any modified dates when extracting from an RCF file.

```text
-preservercftimes
```

# -memory

**Added in version 1.0.**

Load every input file into memory when building an RCF file.

```text
-memory
```
