+++
date = "2016-08-01"
title = "CAST (Data: classes.lst)"
original_url = "/list/data/classes.html#cast"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "CAST"
    parent = "data_classes"
+++

## Status

None

## Syntax

`CAST:x`

## Parameters

-   x: Number or Formula



<span id="cast"></span> \*\*\* Updated 5.8

What it does
------------

-   Tells PCGen how many spell per day the caster has (displayed on the
    Spells Tab).
-   If no Value is assigned at a given level, the tag defaults to 0.
-   **Note:** The formula used cannot have commas (,) embedded in it. If
    a formula requires a comma use a DEFINE to set a variable and use
    the variable in the CAST progression.

Example
-------

`CAST:3,3,1`

Class can cast 3 0th level spells, 3 1st level spells and 1 2nd level
spell.

Example
-------

`DEFINE:CastLvl0|min(6,4+CL) <tab> CAST:CastLvl0`

Sets the cast progression to the value of the variable `CastLvl0` for 0
level spells.

Where it is used
----------------

Class Level Line.

