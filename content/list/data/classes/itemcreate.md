+++
date = "2016-08-01"
title = "ITEMCREATE (Data: classes.lst)"
original_url = "/list/data/classes.html#itemcreate"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "ITEMCREATE (Data: classes.lst)"
    parent = "classes"
+++

## Status

None

## Syntax

`ITEMCREATE:x`

## Parameters

-   Variables Used: Number or formula



What it does
------------

-   This tag provides a multiplier by which the class level of the
    character will be multiplied for calculating potions, scrolls,
    and wands.
-   This tag is optional and if not provided the multiplier used will
    default to a value of 1.

Example
-------

`ITEMCREATE:2`

The class level is doubled when calculating potions, scrolls and wands.

`CLASS:Paladin ITEMCREATE:CL/3.3`

The class level is calculated to the following values at different
Character Levels; 1=.3, 2=.6, 3=.9, 4=1.2, 5=1.5, 6=1.8, 7=2.1, 8=2.4,
9=2.7, 10=3.0 when calculating potions, scrolls and wands.

Where it is used
----------------

Class Line.

