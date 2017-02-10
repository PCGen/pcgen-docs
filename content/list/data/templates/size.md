+++
date = "2016-08-01"
title = "SIZE (Data: templates.lst)"
original_url = "/list/data/templates.html#size"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "SIZE"
    parent = "data_templates"
+++

## Status

Updated 5.11.13

## Syntax

`SIZE:x`

## Parameters

-   x: Text (F,D,T,S,M,L,H,G,C)
-   x: Number or Formula (Numeric value of the
    size value)



What it does
------------

-   Sets the character's size, which is used in determining TO-HIT, AC,
    and affects some skills.
-   Sizes are defined by the numeric values 0 thru 8 and may have
    textual values defined in the appropriate GameMode file. (See Game
    Mode File &gt; Size Adjustment &gt; [SIZENAME
    TAG](/list/system/sizeadjustment/sizename.html) )
-   Note that if a value outside this range is used the result
    is undefined.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `SIZE` tag, the data included in a new `SIZE` tag
    will overwrite the existing tag data.

Example
-------

`SIZE:M`

The character is "Medium" size.

`SIZE:max(AnimalSize,SIZE)`

Sets the character's size to the maximum of the variable "AnimalSize"
and current size.

**.MOD Example:**

Initial Template: `<template name> <tab> SIZE:M`

Modified By: `<template name>.MOD <tab> SIZE:L`

Is Equivalent To: `<template name> <tab> SIZE:L`

The creatue is "Large".

