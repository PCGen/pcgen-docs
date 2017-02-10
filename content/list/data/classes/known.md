+++
date = "2016-08-01"
title = "KNOWN (Data: classes.lst)"
original_url = "/list/data/classes.html#known"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "KNOWN"
    parent = "data_classes"
    identifier = "data_classes_KNOWN"
+++

## Status

None

## Syntax

`KNOWN:x`

## Parameters

-   x: Number



<span id="known"></span> \*\*\* Updated 5.8

What it does
------------

-   Tells PCGen how many spell known the caster has (displayed on the
    Spells Tab).
-   If no Value is assigned at a given level, the tag defaults to 0.
-   **Note:** The formula used cannot have commas (,) embedded in it. If
    a formula requires a comma use a DEFINE to set a variable and use
    the variable in the KNOWN progression.

Example
-------

`KNOWN:6,4,3`

The class knows 6 0th level spells, 4 1st level spells and 3 2nd level
spells.

Example
-------

`DEFINE:KnownLvl0|min(9,4+(CL/2)) <tab> KNOWN:KnownLvl0`

Sets the known progression to the value of the variable `KnownLvl0` for
0 level spells.

Where it is used
----------------

Class Level Line.

