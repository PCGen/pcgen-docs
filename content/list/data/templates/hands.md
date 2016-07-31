+++
date = "2016-08-01"
title = "HANDS (Data: templates.lst)"
original_url = "list/data/templates.html#hands"
categories = [ "all-tag", "templates-tag" ]
+++

## Status

None

## Syntax

`HANDS:x`

## Parameters

-   x: Number (Number of Hands &gt;= 0)



What it does
------------

-   Determines the number of hands the creature has for purposes of
    multiattacks and multidexterity.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `HANDS` tag, the data included in a new `HANDS`
    tag will overwrite the existing tag data.

Example
-------

`HANDS:4`

The creature has four hands.

**.MOD Example:**

Initial Template: `Darkling Sorcerer <tab> HANDS:2`

Modified By: `Darkling Sorcerer.MOD <tab> HANDS:4`

Is Equivalent To: `Darkling Sorcerer <tab> HANDS:4`

The Darkling Sorcerer's number of hands is set to "4".

