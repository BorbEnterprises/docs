---
title: AddCondition
description: Adds a condition for failing to a mission stage.
authors: ["loren"]
---

This command adds a condition for failing to a mission stage.

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

Additionally, this should be followed by a call to [CloseCondition](closecondition.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddCondition( condition_type, [keepbarrel_fail_stage_count] );
```
{{ endtab }}
{{ tab Lua }}
```lua
AddCondition( condition_type, [keepbarrel_fail_stage_count] );
```
{{ endtab }}
{{ endtabs }}

* **type**: The type of [condition](../conditions/all-conditions.md) to add.
* **keepbarrel_fail_stage_count**: The number of stages to go back when failing a [keepbarrel](../conditions/keepbarrel.md) condition.

# Examples
{{ snippet hitandrun/mfk-commands/timeout-condition-example }}

# Notes
No additional notes.