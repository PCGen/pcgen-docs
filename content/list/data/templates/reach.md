+++
date = "2016-08-01"
title = "REACH (Data: templates.lst)"
original_url = "/list/data/templates.html#reach"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "REACH"
    parent = "data_templates"
+++

## Status

None

## Syntax

`REACH:x`

## Parameters

-   x: Number (Reach in Feet &gt;= 0)



What it does
------------

-   Changes the creature's reach.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `REACH` tag, the data included in a new `REACH`
    tag will overwrite the existing tag data.

Example
-------

`REACH:10`

The creature has a reach of ten (10) feet.

**.MOD Example:**

Initial Template: `<template name> <tab> REACH:10`

Modified By: `<template name>.MOD <tab> REACH:20`

Is Equivalent To: `<template name> <tab> REACH:20` .

The character's reach is now twenty (20) feet.

