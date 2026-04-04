---
title: "Creating Your First Server Mod"
description: "A guide to creating your first Simpsons Hit & Run Multiplayer Server mod."
authors: [ 1 ]
---

This guide will walk you through creating a simple server-side mod that welcomes players when they join.

# Prerequisites

* A running Simpsons Hit & Run Multiplayer Server with `enableMods: true` in `Server.yaml` (this is the default). See [[SettingUpOnWindows.md]] or [[SettingUpOnLinux.md]] if you haven't set one up yet.

# Step 1: Create a Mod Folder

Inside the `ServerMods` folder (located next to your server executable), create a new folder for your mod. The folder name should match your mod's internal name.

```
ServerMods/
└── MyFirstMod/
```

# Step 2: Create Mod.yaml

Inside your mod folder, create a `Mod.yaml` file. This file describes your mod to the server.

```yaml
internalName: MyFirstMod
title: My First Mod
description: A simple welcome message mod.
version: 1.0.0
entryPoint: Main.lua
```

| Field          | Description                                                        |
|----------------|--------------------------------------------------------------------|
| `internalName` | A unique identifier for your mod. Should match the folder name.    |
| `title`        | The display name of your mod.                                      |
| `description`  | A short description of what your mod does.                         |
| `version`      | The version of your mod.                                           |
| `entryPoint`   | The Lua script that the server will run when loading your mod.     |

# Step 3: Create the Entry Point Script

Create a `Main.lua` file inside your mod folder. This is the script that runs when your mod is loaded.

```lua
Server.AddEventListener("PlayerJoined", function(e)
    local player = e.Client

    player:SendGameChatMessage("Welcome to " .. Server.Config.ServerName .. ", " .. player.Name .. "!")
end)
```

This script listens for the `PlayerJoined` event and sends a welcome message in the in-game chat to each player when they connect.

Your mod folder should now look like this:

```
ServerMods/
└── MyFirstMod/
    ├── Mod.yaml
    └── Main.lua
```

# Step 4: Start the Server

Start (or restart) your server. The server will automatically discover and load your mod from the `ServerMods` folder.

# Next Steps

* See [[../LuaScripting.md]] for a full reference of all tables and functions available in server mods.
* See [[../LuaScripting/Events.md]] for a full list of events you can listen for.
