+++
date = "2016-08-01"
title = "SUBREGION (Data: templates.lst)"
original_url = "list/data/templates.html#subregion"
categories = [ "all-tag", "templates-tag" ]
+++

## Status

None

## Syntax

`SUBREGION:x`

## Parameters

-   x: Text (Sub-Region Name)
-   x: YES



What it does
------------

-   This sets the name of the sub-region the character is from. The
    default sub-region is none.
-   If "YES" is specified then it will place the name of the template in
    parenthesis after the region on character sheet output.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `SUBREGION` tag, the data included in a new
    `SUBREGION` tag will overwrite the existing tag data.

Example
-------

`SUBREGION:South Side`

The character is from the "South Side" subregion.

**.MOD Example:**

Initial Template: `South Philly <tab> SUBREGION:South Side`

Modified By: `South Philly.MOD <tab> SUBREGION:Philadelphia`

Is Equivalent To: `South Philly <tab> SUBREGION:Philadelphia` .

The character is from "Philadelphia".

