+++
date = "2016-08-01"
title = "REMOVABLE (Data: templates.lst)"
original_url = "/list/data/templates.html#removable"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "REMOVABLE"
    parent = "data_templates"
+++

## Status

None

## Syntax

`REMOVABLE:x`

## Parameters

-   x: Boolean (YES or NO)



What it does
------------

-   This denotes whether a character can remove a template once it
    is chosen.
-   If this tag is not included the default value is **YES** .
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `REMOVABLE` tag, the data included in a new
    `REMOVABLE` tag will overwrite the existing tag data.

Example
-------

`REMOVABLE:NO`

The template may not be removed if taken.

`<template name>.MOD <tab> REMOVABLE:YES`

The template may be removed after being taken.

**.MOD Example:**

Initial Template: `<template name> <tab> REMOVABLE:NO`

Modified By: `<template name>.MOD <tab> REMOVABLE:YES`

Is Equivalent To: `<template name> <tab> REMOVABLE:YES`

The template is removable.

