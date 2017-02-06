+++
date = "2016-08-01"
title = "NONPP (Data: templates.lst)"
original_url = "/list/data/templates.html#nonpp"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "NONPP (Data: templates.lst)"
    parent = "templates"
+++

## Status

None

## Syntax

`NONPP:x`

## Parameters

-   x: Number (Non-proficiency penalty &lt;= 0)



What it does
------------

-   Sets he character's penalty for non-proficiency in a weapon to the
    number specified.
-   The number specified must be less-than or equal to zero (0).
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `NONPP` tag, the data included in a new `NONPP`
    tag will overwrite the existing tag data.

Example
-------

`NONPP:-2`

The non-proficiency penalty is minus two.

**.MOD Example:**

Initial Template: `<template name> <tab> NONPP:-2`

Modified By: `<template name>.MOD <tab> NONPP:-1`

Is Equivalent To: `<template name> <tab> NONPP:-1` .

The non-proficiency penalty is minus one.

