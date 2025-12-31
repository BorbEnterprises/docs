---
title: Introduction
description: "The Donut Team API allows developers to retrieve basic information about donut team releases and users via HTTP requests."
authors: ["jake","loren"]
---

The Donut Team API allows developers to retrieve basic information about Donut Team releases (Apps) and users via HTTP requests. 

It does **not** provide any way of authenticating or interacting with user accounts.

This API has no authentication so you can get started right away by sending requests to its various endpoints.

# Supported Formats
The API supports returning both JSON and XML from all of it's endpoints.

## JSON
JSON is the default format that the API will return data in. While not necessary, you can explicitly specify you'd like JSON with `&Format=JSON`.

## XML
XML was added in 1.0.32. You can access it by specifying `&Format=XML`.

# Endpoints

{{ summary donut-team-api/v1/endpoints/applookup | 2 | Learn more... }}
{{ summary donut-team-api/v1/endpoints/profilelookup | 2 | Learn more... }}
{{ summary donut-team-api/v1/endpoints/version | 2 | Learn more... }}