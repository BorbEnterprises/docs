Added **Physics > Baby Van Tilt**. This fixes a famous bug that most notably causes the baby van in Level 5 Mission 3 to be tilted and have incorrect physics. 

This bug as well as this fix both apply to other cars as well though it appears most prominently on this one so it's named after it.

We also added a `FixUninitialisedArticulatedPhysicsObjectCloneRelativeCentreOfMassAndInertiaMatrixUpdateInterval` property to the `[Physics]` section of BugFixes.ini so mods can opt into this bug fix. The name is very literal.

This bug fix exists as a result of extensive research done by aldelaro5. He also made an in depth video explaining the bug which can be found [here](https://www.youtube.com/watch?v=u5J8hZgTuW4) if you're interested.