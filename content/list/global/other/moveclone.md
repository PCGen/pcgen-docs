+++
date = "2016-08-01"
title = "MOVECLONE (Global: OTHER)"
original_url = "/list/global/other.html#moveclone"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "MOVECLONE"
    parent = "global_other"
    identifier = "global_other_MOVECLONE"
+++

## Status

None

## Syntax

`MOVECLONE:x,y,z`

## Parameters

-   x: Text (1st movement mode)
-   y: Text (2nd movement mode)
-   z: Formula (Calculation for 2nd mode movement rate)



What it does
------------

-   Creates a new type of movement based on another type.
-   "z" is applied to the original movement rate, then it is copied to
    the new movement type.
-   If no symbol is in the mathematical expression then addition is
    assumed

Examples
--------

`MOVECLONE:Walk,Fly,*2`

Create the "Fly" movement type and set it equal to "Walk" multiplied by
2.

`MOVECLONE:Walk,Tunnel,/3`

Create "Tunnel" movement type and set it equal to 1/3 of the "Walk"
movement rate.

