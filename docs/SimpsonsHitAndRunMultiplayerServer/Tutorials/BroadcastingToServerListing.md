---
title: "Broadcasting to the Server Listing"
description: "A guide to broadcasting your Simpsons Hit & Run Multiplayer Server to the Donut Team server listing."
authors: [ 1 ]
---

This guide will walk you through broadcasting your server to the Donut Team server listing, making it publicly discoverable on [launcher.donutteam.com](https://launcher.donutteam.com).

# Prerequisites

* A running Simpsons Hit & Run Multiplayer Server. See [[SettingUpOnWindows.md]] or [[SettingUpOnLinux.md]] if you haven't set one up yet.
* A Donut Team account at [donutteam.com](https://donutteam.com).
* Your server must be able to communicate with `launcher.donutteam.com` over HTTPS.
* Your server must be reachable on the same port as your game server (default: `7777`) over TCP. If your server is behind a NAT, you will need to set up port forwarding for that port.

# Step 1: Get Your Authorisation Token

1. Log in to your Donut Team account at [donutteam.com](https://donutteam.com).
2. Navigate to your account authentication settings at [donutteam.com/settings/authentication](https://donutteam.com/settings/authentication).
3. Copy the token from the **Token** section.

# Step 2: Configure Your Server

Open your `Server.yaml` file and set the following options:

```yaml
masterServerAuthorisation: 'your-token-here'
broadcastServer: true
```

See [[../Configuration.md]] for a full description of these options.

# Step 3: Restart Your Server

Restart the server for the changes to take effect. Once running, your server will register itself with the Donut Team master server and appear in the server listing at [launcher.donutteam.com](https://launcher.donutteam.com).

You can also toggle broadcasting at runtime without restarting using the `/broadcast-server` command:

```
/broadcast-server true
/broadcast-server false
```
