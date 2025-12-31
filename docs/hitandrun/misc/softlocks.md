---
title: Softlocks
description: "This page documents some ways to softlock the game."
---

This page documents some ways to softlock the game.

# Modded
These softlocks require you to create a mod that introduces the circumstances required for the softlock to occur.

## Invalid Dialogue Stage Placement
Defining a dialogue stage after a stage marked as the final stage will cause the dialogue stage to behave in an abnormal manner:

* The normal letterboxing shown in a dialogue stage will not be displayed.
* It is not possible to skip or cancel the dialogue.
* It is possible to pause during the dialogue where it normally is not.
* The player will be locked in place after the dialogue is over until they pause and unpause the game (this can be done during the dialogue as mentioned above).
   
At this point, it is impossible to pass the stage without using hacks to bypass it. Any subsequent stages will be impossible to reach.

```js
// If this is done in a regular mission, this stage will not cause the Mission Complete text to appear like it normally would.
AddStage("final");
	AddObjective("timer");
		SetDurationTime(1);
	CloseObjective();
CloseStage();

// This stage will play the specified dialogue with the aforementioned oddities.
AddStage(1);
	AddObjective("dialogue");
		...
	CloseObjective();
CloseStage();

// This stage will never get reached.
// However, if it is reached with hacks it will complete as normal.
AddStage();
	AddObjective("timer");
		SetDurationTime(1);
	CloseObjective();
CloseStage();
```

A video showcasing this softlock can be found [here](https://www.youtube.com/watch?v=Ajti0DfjOnE).