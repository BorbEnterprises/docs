---
title: ProfileLookup
description: "This endpoint provides basic information about a user."
authors: ["jake", "loren"]
---

This endpoint provides basic information about Donut Team users.

# Endpoint
```text
https://api.donutteam.com/?Event=ProfileLookup
```

# Arguments
## MethodOfAccessingUserInformation

| Values   | Result                                                                |
|----------|-----------------------------------------------------------------------|
| username | Looks up the specified user(s) by username                            |
| discord  | Looks up the specified user(s) by their Discord ID                    |
| id       | Default Value - Looks up the specified user(s) by their Donut Team ID |

## Users
A list of usernames, discord IDs or Donut Team IDs separated by colons.

```text
&Users=2:9:395
```

# Example Responses
{{ tabs }}
{{ tab JSON (Default) }}
```text
GET https://api.donutteam.com/?Event=ProfileLookup&MethodOfAccessingUserInformation=id&Users=2:9:395
```
```json
{
    "2": {
        "Id": 2,
        "Username": "loren",
        "DisplayName": "Loren",
        "Rank": 5,
        "JoinDate": 1363694400,
        "IsConfirmed": true,
        "Banned": false
    },
    "9": {
        "Id": 9,
        "Username": "Cornholio309",
        "DisplayName": "Kenny Giles",
        "Rank": 5,
        "JoinDate": 1363694400,
        "IsConfirmed": true,
        "Banned": false
    },
    "395": {
        "Id": 395,
        "Username": "lucasc190",
        "DisplayName": "Lucas Cardellini",
        "Rank": 5,
        "JoinDate": 1396234333,
        "IsConfirmed": true,
        "Banned": false
    }
}
```
{{ endtab }}
{{ tab XML }}
```text
https://api.donutteam.com/?Event=ProfileLookup&MethodOfAccessingUserInformation=id&Users=2:9:395&Format=XML
```
```xml
<DonutTeamAPI>
	<Data Value="2">
		<Id>2</Id>
		<Username>loren</Username>
		<DisplayName>Loren</DisplayName>
		<Rank>5</Rank>
		<JoinDate>1363694400</JoinDate>
		<IsConfirmed>1</IsConfirmed>
		<Banned/>
	</Data>
	<Data Value="9">
		<Id>9</Id>
		<Username>Cornholio309</Username>
		<DisplayName>Kenny Giles</DisplayName>
		<Rank>5</Rank>
		<JoinDate>1363694400</JoinDate>
		<IsConfirmed>1</IsConfirmed>
		<Banned/>
	</Data>
	<Data Value="395">
		<Id>395</Id>
		<Username>lucasc190</Username>
		<DisplayName>Lucas Cardellini</DisplayName>
		<Rank>5</Rank>
		<JoinDate>1396234333</JoinDate>
		<IsConfirmed>1</IsConfirmed>
		<Banned/>
	</Data>
</DonutTeamAPI>
```
{{ endtab }}
{{ endtabs }}

# Notes

* This endpoint has some strange gotchas when `Format` is set to `XML` that will **not** be changed for backwards compatibility and should be kept in mind:
	* `IsConfirmed` will be represented as `0` or `1` rather than `false` or `true.
	* An empty `<Banned />` element will be returned if the user is *not* banned and `<Banned>1</Banned>` will be returned if they are.