---
title: timeout
description: "Fails the player if they run out of time in a stage."
authors: ["loren"]
---

This type of condition fails the player if they run out of time in the stage.

# Examples
{{ snippet hitandrun/mfk-commands/timeout-condition-example }}

# Notes
This condition will immediately fail the player if the stage doesn't contain a call to [SetStageTime](../mfk-commands/setstagetime.md) or [AddStageTime](../mfk-commands/addstagetime.md).