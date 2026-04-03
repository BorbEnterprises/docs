---
title: "JSON.Encode"
description: "Provides information about the JSON.Encode function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 528 # 1.1
---

Encodes a Lua value as a JSON string. Tables with sequential integer keys starting at `1` are encoded as JSON arrays; all other tables are encoded as JSON objects.

# Syntax
```lua
JSON.Encode( value )
```

## Arguments
* **value** (any): The value to encode. Supported types are `table`, `boolean`, `number`, `string`, and `nil`.

## Return Values
* (string): A JSON string representation of the value.

# Examples
```lua
local json = JSON.Encode({ name = "Homer", level = 1 })
print(json) -- Outputs: {"name":"Homer","level":1}
```

```lua
local json = JSON.Encode({ "a", "b", "c" })
print(json) -- Outputs: ["a","b","c"]
```
