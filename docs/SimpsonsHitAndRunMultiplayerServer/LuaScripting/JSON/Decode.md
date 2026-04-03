---
title: "JSON.Decode"
description: "Provides information about the JSON.Decode function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 528 # 1.1
---

Decodes a JSON string into a Lua value. JSON objects and arrays are returned as tables. JSON arrays use sequential integer keys starting at `1`. Returns `nil` if the input string is empty or whitespace.

# Syntax
```lua
JSON.Decode( json )
```

## Arguments
* **json** (string): The JSON string to decode.

## Return Values
* (table | string | number | boolean | `nil`): The decoded Lua value, or `nil` if the input is empty or whitespace.

# Examples
```lua
local result = JSON.Decode('{"name":"Homer","level":1}')
print(result.name)  -- Outputs: Homer
print(result.level) -- Outputs: 1
```

```lua
local result = JSON.Decode('["a","b","c"]')
print(result[1]) -- Outputs: a
print(result[2]) -- Outputs: b
```
