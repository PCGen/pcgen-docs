+++
date = "2016-08-01"
title = "AGESET (System: bio/biosettings.lst)"
original_url = "/list/system/biosettings.html#ageset"
categories = [ "all-tag", "biosettings-tag" ]
[menu.main]
    name = "AGESET"
    parent = "system_biosettings"
+++

## Status

None

## Syntax

`AGESET:x|y`

## Parameters

-   x: Number (The number of the age set)
-   y: Text (A name for the age set - Adult, Old,
    Venerable, etc.)



What it does
------------

-   Defines the age ranges for each race and age category.
-   Each age category should have it's own AGESET tag with a different
    Text field for a name.
-   Each AGESET tag should be sequentially numbered starting at 0, for
    the youngest age category.

Examples
--------

`AGESET:0|Adulthood`

1st ageset is "Adulthood".

`AGESET:1|Middle Age`

2nd ageset is "Middle Age".

