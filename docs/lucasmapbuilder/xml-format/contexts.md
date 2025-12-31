---
title: Contexts
description: Contexts are scopes for various elements defined in XML files.
status:
    class: "wip"
---

Contexts are scopes for various elements defined in XML files.

This means that the context something is defined within controls where else it can be used.

The following things are context-specific:

* Global Variables
* Local Variables
* Local Named Elements
    * [ModelOutputInstructions](elements/outputs/modeloutputinstructions.md)
* Ignored Warnings
* Included Warnings

The following XML Elements allow you to control the context of these things:

* [Build XML Element](elements/general/build.md)
* [Include XML Element](elements/general/include.md)
* [Context XML Element](elements/general/context.md)
* [SetVariable XML Element](elements/general/setvariable.md)