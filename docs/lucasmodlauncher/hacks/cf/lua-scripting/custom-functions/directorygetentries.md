---
title: DirectoryGetEntries
description: "Calls a callback function for every file and sub-directory in the given path."
---

Calls a callback function for every file and sub-directory in the given path.

The order of these files is not predictable and should not be relied upon.

# Syntax
```lua
DirectoryGetEntries( <path>, <callback>, [<end_to_start>] )
```

* **path**: The directory to iterate.
* **callback**: The callback that will be called for each item in the directory. 
    * This callback is given the two arguments:
        * **FileOrDirectory**: The file or directory name.
        * **IsDirectory**: Whether or not the entry is a directory.
    * This callback must return true for the loop to continue.
* **end_to_start**: Makes the function iterate the directory in reverse order. 
    * Optional, defaults to false.

# Examples
```lua
-- Print each file and whether or not it's a directory.
DirectoryGetEntries(Path, function(FileOrDirectory, IsDirectory)
    print(FileOrDirectory, IsDirectory)

    return true
end)
```

# Notes
No additional notes.

# Version History
## 1.23.10
Fixed a bug where calling `DirectoryGetEntries` on `/` yielded no results (when not using the `-legacyfilesystem` command line argument).

## 1.18
Added a third argument that specifies whether or not to return the list of files and folders in reverse order.

## Unknown Version
Added this function.