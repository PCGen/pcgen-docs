+++
date = "2016-08-01"
title = "HITDIE (Data: classes.lst)"
original_url = "/list/data/classes.html#hitdie"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "HITDIE (Data: classes.lst)"
    parent = "classes"
+++

## Status

None

## Syntax

`HITDIE:x`

## Parameters

-   x: Number (Hit Die size)
-   x: %+Number (Amount added to Hit Die)
-   x: %-Number (Amount subtracted from Hit Die)
-   x: %\*Number (Amount Hit Die is multiplied by)
-   x: %/Number (Amount Hit Die is divided by)
-   x: %upNumber (Amount Hit Die size is stepped up by)
-   x: %downNumber (Amount Hit Die size is stepped
    down by)
-   x: %HupNumber (Amount Hit Die size is stepped
    up by)
-   x: %HdownNumber (Amount Hit Die size is stepped
    down by)



<span id="hitdie"></span> \*\*\* Updated 5.13.6

What it does
------------

-   This tag can be used on a Class level line, a
    [SUBCLASSLEVEL](/list/data/classes/subclasslevel.html) line or a
    [SUBSTITUTIONLEVEL](/list/data/classes/substitutionlevel.html) line
    to specify a Hit Die size which will be applied only that level.
-   The scale used by the functions which raise or lower Hit Die in
    steps is defined by the
    [DIESIZES](/list/system/gamemode-miscinfo/diesizes.html)
    gameMode tag.
-   The scale used in most gameModes is:
    1,2,3,MIN=4,6,8,10,MAX=12,20,100,1000
-   When using the step up function (%upNumber) or step down
    function (%downNumber) the minimum and maximum steps are set by the
    MIN and MAX tags in the DIESIZES tag.
-   The step up function (%Hup) and step down functions (%Hdown) will
    ignore the MIN and MAX settings and use the full range of die sizes
    specified by the DIESIZES tag.
-   Regardless of the number it will never allow a hit die below 1.
-   HITDIE may also be used in [Race](/list/data/races/hitdie.html) and
    [Template](/list/data/templates/hitdie.html) files.

Example
-------

`HITDIE:12`

The character now has a Hit Dice of 12.

`HITDIE:%+2`

Adds 2 to the current Hit Dice size.

`HITDIE:%-4`

Subtracts 4 from the current Hit Dice size.

`HITDIE:%*3`

Multiplies the current Hit Dice size by 3.

`HITDIE:%/2`

Divides the current Hit Dice size by 2.

`HITDIE:%up2`

Steps up the Hit Dice size by two steps. If the class has a Hit Die of
d6 it will be stepped up to d10.

`HITDIE:%down1`

Steps down the Hit Dice size by one step. If the class has a Hit Die of
d6 it will be stepped down to d4.

`HITDIE:%Hup4`

Steps up the Hit Dice size by four steps. If the class has a Hit Die of
d6 it will be stepped up to d20.

`HITDIE:%Hdown3`

Steps down the Hit Dice size by three step. If the class has a Hit Die
of d6 it will be stepped down to d2.

Where it is used
----------------

Class Level Line.

