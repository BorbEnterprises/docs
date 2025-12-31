---
title: Version
description: "This endpoint provides the current API version."
authors: ["jake", "loren"]
---

This endpoint provides information about the current API version.

# Endpoint
```text
https://api.donutteam.com/
https://api.donutteam.com/?Event=Version
```

# Arguments
## Accessor
The user accessing the endpoint. This is optional and is purely for logging purposes.

```
?Accessor=Loren
```

# Example Response
{{ tabs }}
{{ tab JSON (Default) }}
```text
https://api.donutteam.com/
```
```json
{
    "Accessor": "Unidentified Developer",
    "Method": "GET",
    "Event": "Version",
    "Version": "1.1.50-hack"
}
```
{{ endtab }}
{{ tab XML }}
```text
https://api.donutteam.com/?Format=XML
```
```xml
<?xml version="1.0"?>
<DonutTeamAPI>
	<Accessor>Unidentified Developer</Accessor>
	<Method>GET</Method>
	<Event>Version</Event>
	<Version>1.1.50-hack</Version>
</DonutTeamAPI>
```
{{ endtab }}
{{ tab Accessor }}
```text
https://api.donutteam.com/?Accessor=Loren
```
```json
{
    "Accessor": "Loren",
    "Method": "GET",
    "Event": "Version",
    "Version": "1.1.50-hack"
}
```
{{ endtab }}
{{ endtabs }}