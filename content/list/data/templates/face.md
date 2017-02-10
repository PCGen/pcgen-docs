+++
date = "2016-08-01"
title = "FACE (Data: templates.lst)"
original_url = "/list/data/templates.html#face"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "FACE"
    parent = "data_templates"
    identifier = "data_templates_FACE"
+++

## Status

None

## Syntax

`FACE:x,y`

## Parameters

-   x: Number (Space the creature occupies &gt;= 0)
-   y: Number (Optional, side space &gt;= 0)



What it does
------------

-   Describes how much space the creature takes up.
-   If only one number is used it is assumed to represent all sides.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `FACE` tag, the data included in a new `FACE` tag
    will overwrite the existing tag data.

NOTE: For the SRD (3e), this tag is used for the Face statistic. For 3.5
rules this tag is used for the Space statistic.

Example
-------

`FACE:5,10`

The creature has a face/space of 5 by 10.

`FACE:10`

The creature has a face/space of 10.

`<template name>.MOD <tab> FACE:20`

The creature has a face/space of 20.

**.MOD Example:**

Initial Template: `Darkling <tab> FACE:10,5`

Modified By: `Darkling.MOD <tab> FACE:10`

Is Equivalent To: `Darkling <tab> FACE:10`

Darklings have a "face/space" of "10".

