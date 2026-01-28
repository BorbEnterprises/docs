* Added support for encrypting mods when compiling them.
    * This is enabled by default for mods that require this version or newer but it can also be opted into manually (which will also implicity make the mod require this version or newer).
    * This only encrypts text based files (.ini, .xml, .lua, .con, .mfk, .cho, .spt) by default.
        * Various new properties were added to the `[Compile]` section of mods to configure what gets encrypted.
    * Also added a `-forceencryption` command line argument so the Mod Launcher will always encrypt mods regardless of their RequiredLauncher or other criteria.