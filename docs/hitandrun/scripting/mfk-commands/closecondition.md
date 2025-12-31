---
title: CloseCondition
description: "Closes a condition added with AddCondition."
authors: ["loren"]
---

This command closes a condition added with [AddCondition](addcondition.md).

# Context
{{ snippet hitandrun/command-contexts/mission-init-stage }}

Additionally, this should only be called after a call to [AddCondition](addcondition.md).

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ snippet hitandrun/mfk-commands/timeout-condition-example }}

# Notes
No additional notes.