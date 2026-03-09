---
title: "DateTime.date"
description: "Provides information about the DateTime.date function available in Simpsons Hit & Run Multiplayer Server mods."
authors: [ 1 ]
initialVersion:
  project_id: 124 # Simpsons Hit & Run Multiplayer (SHAR MP) Server
  projectBranch_id: 165 # Main Branch
  projectBranchVersion_id: 441 # 1.0
---

Returns a formatted date string based on the provided format string and the current date and time.

# Syntax
```lua
DateTime.date( format )
```

## Arguments
* **format** (string): A format string that specifies how the date should be formatted. The format string can contain the following placeholders:
  * `%Y`: Year with century (e.g., 2021)
  * `%m`: Month as a zero-padded decimal number (01-12)
  * `%d`: Day of the month as a zero-padded decimal number (01-31)
  * `%H`: Hour (24-hour clock) as a zero-padded decimal number (00-23)
  * `%M`: Minute as a zero-padded decimal number (00-59)
  * `%S`: Second as a zero-padded decimal number (00-59)

## Return Values
(string): The formatted date string.

# Examples
```lua
local formattedDate = DateTime.date("%Y-%m-%d %H:%M:%S")
print(formattedDate) -- Outputs: 2026-01-01 12:34:56 (example output, will vary based on current date and time)
```