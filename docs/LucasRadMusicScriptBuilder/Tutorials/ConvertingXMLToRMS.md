---
title: "Building RadMusic Scripts from XML"
description: "These are 2 different methods of building RMS files from XML with the RMS builder."
---

These are 2 different methods of building RMS files from XML with the RMS builder.

# Method 1 (Simple)
The simplest way to build a RadMusic Script from an XML file is to drag the XML file onto the RMS Builder's executable. This will build an RMS file of the same name next to your XML file.

**NOTE 1:** This method requires your XML files to be in your Mod's sound\music folder if you don't want to manually move the RMS file there each time you build it. If you want to keep them separate, see Method 2 below.

**NOTE 2:** If your mod has custom music, you will need to use Method 2 in order to specify the `-rsdpath` command line argument.

# Method 2 (Complex)
You may want to keep your XML files somewhere other than your Mod's sound\music folder. You can do this using command line arguments to tell the RMS builder where to build the output RMS file.

We recommend doing this with a batch file. You'll need to use the `-inputxml`, `-outputrms` and `-rsdpath` command line arguments. You'll need to adjust these paths to your specific setup but here's an example:

```text
@"C:\path\to\LRMSB.exe" -inputxml "%~dp0Build.xml" -outputrms "C:\path\to\YourMod\CustomFiles\sound\music\l1_music.rms" -rsdpath "C:\path\to\YourMod\CustomFiles\sound\music"
```