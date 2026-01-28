* Made Lens Flares not get enqueued if their World Sphere is deactivated.
    * Also added the `-deactivatedworldspherelensflares` command line argument to suppress this behaviour.
    * This fixes an issue where deactivating a world sphere would not deactivate its lens flare.