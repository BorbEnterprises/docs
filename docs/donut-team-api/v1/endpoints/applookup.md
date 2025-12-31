---
title: AppLookup
description: "This endpoint provides basic information about a submitted application."
authors: ["jake", "loren"]
---

This endpoint provides basic information about Donut Team releases.

# Endpoint
```text
https://api.donutteam.com/?Event=AppLookup
```

# Arguments
## Apps
A list of app IDs separated by colons.

```text
&Apps=1:4
```

# Example Response
{{ tabs }}
{{ tab JSON (Default) }}
```text
GET https://api.donutteam.com/?Event=AppLookup&Apps=1:4
```
```json
{
    "1": {
        "Title": "Donut Mod 3",
        "Version": "3.2.3",
        "Category": 0,
        "ChangelogLink": "https://docs.donutteam.com/docs/donutmod/versions/version_3.2.3",
        "DonutTeamDownloadLink": "https://donutteam.com/downloads/1/"
    },
    "4": {
        "Title": "Lucas' Simpsons Hit & Run Mod Launcher",
        "Version": "1.26.1",
        "Category": 0,
        "ChangelogLink": "https://docs.donutteam.com/docs/lucasmodlauncher/versions/version_1.26.1",
        "DonutTeamDownloadLink": "https://donutteam.com/downloads/4/"
    }
}
```
{{ endtab }}
{{ tab XML }}
```text
GET https://api.donutteam.com/?Event=AppLookup&Apps=1:4&Format=XML
```
```xml
<DonutTeamAPI>
	<Data Value="1">
		<Title>Donut Mod 3</Title>
		<Version>3.2.3</Version>
		<Category>0</Category>
		<ChangelogLink>https://docs.donutteam.com/docs/donutmod/versions/version_3.2.3</ChangelogLink>
		<DonutTeamDownloadLink>https://donutteam.com/downloads/1/</DonutTeamDownloadLink>
	</Data>
	<Data Value="4">
		<Title>Lucas' Simpsons Hit &amp; Run Mod Launcher</Title>
		<Version>1.26.1</Version>
		<Category>0</Category>
		<ChangelogLink>https://docs.donutteam.com/docs/lucasmodlauncher/versions/version_1.26.1</ChangelogLink>
		<DonutTeamDownloadLink>https://donutteam.com/downloads/4/</DonutTeamDownloadLink>
	</Data>
</DonutTeamAPI>
```
{{ endtab }}
{{ endtabs }}