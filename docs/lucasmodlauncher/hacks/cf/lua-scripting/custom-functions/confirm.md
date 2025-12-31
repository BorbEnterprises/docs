---
title: Confirm
description: "Shows a Windows message box with an \"OK\" button and a \"Cancel\" button for debugging purposes."
---

Shows a Windows message box with an "OK" button and a "Cancel" button for debugging purposes.

This returns true if "OK" was pressed and false if "Cancel" was pressed.

# Syntax

```lua
Confirm( <message> )
```

* **message**: The message to show in message box.

# Examples
```lua
local Result = Confirm("Something, something, skulls on Barts car.") 

if Result then
	-- User clicked OK
else
	-- User clicked Cancel
end
```

# Notes
No additional notes.

# Version History
## Unknown Version
Added this function.