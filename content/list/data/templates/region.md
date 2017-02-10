+++
date = "2016-08-01"
title = "REGION (Data: templates.lst)"
original_url = "/list/data/templates.html#region"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "REGION"
    parent = "data_templates"
+++

## Status

None

## Syntax

`REGION:x`

## Parameters

-   x: Text (Region name)
-   x: YES (Not case sensitive)



What it does
------------

-   This sets the name of the region the character is from, the default
    is none.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `REGION` tag, the data included in a new `REGION`
    tag will overwrite the existing tag data.

Example
-------

`REGION:Timbuktu`

The character is from "Timbuktu".

**.MOD Example:**

Initial Template: `<template name> <tab> REGION:Timbuktu`

Modified By: `<template name>.MOD <tab> REGION:Saskatewan`

Is Equivalent To: `<template name> <tab> REGION:Saskatewan` .

The character is from "Saskatewan".

