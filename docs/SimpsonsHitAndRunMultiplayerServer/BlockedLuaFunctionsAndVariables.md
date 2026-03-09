---
title: "Blocked Lua Functions and Variables"
description: "Lists all of the stock Lua functions and variables that are blocked in Simpsons Hit & Run Multiplayer Server."
authors: [ 1 ]
---

The following stock Lua functions and variables are blocked in Simpsons Hit & Run Multiplayer Server for security and stability reasons.

# io 
The `io` library is blocked to prevent mods from performing file input/output operations that could potentially harm the server or access sensitive data. Use [[LuaScripts/File.md]] instead.

# debug
The `debug` library is blocked to prevent mods from accessing the Lua debug API, which could be used to manipulate the execution of the server or access sensitive information.

# os
The following functions from the `os` library are blocked:
* `os.execute` - Executes a shell command. This is blocked to prevent mods from executing arbitrary commands on the server.
* `os.exit` - Terminates the Lua script. This is blocked to prevent mods from accidentally or intentionally terminating the server.
* `os.getenv` - Retrieves the value of an environment variable. This is blocked to prevent mods from accessing sensitive environment variables.
* `os.remove` - Deletes a file. This is blocked to prevent mods from deleting important files on the server. Use [[LuaScripts/File/Delete.md]] instead.
* `os.rename` - Renames a file. This is blocked to prevent mods from renaming important files on the server. Use [[LuaScripts/File/Write.md]] to write to a new file and then delete the old file if needed.
* `os.tmpname` - Generates a temporary file name. This is blocked to prevent mods from creating temporary files that could clutter the server's file system or be used for malicious purposes.
* `os.setlocale` - Sets the current locale. This is blocked to prevent mods from changing the locale settings of the server, which could affect the behavior of other mods or the server itself.
