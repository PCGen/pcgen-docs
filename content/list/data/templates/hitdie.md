+++
date = "2016-08-01"
title = "HITDIE (Data: templates.lst)"
original_url = "/list/data/templates.html#hitdie"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "HITDIE (Data: templates.lst)"
    parent = "templates"
+++

## Status

Updated 5.13.6

## Syntax

`HITDIE:x|y`

## Parameters

-   x: Number (Hit Die size)
-   x: %+Number (Amount added to Hit Die)
-   x: %-Number (Amount subtracted from Hit Die)
-   x: %\*Number (Amount Hit Die is multiplied by)
-   x: %/Number (Amount Hit Die is divided by)
-   x: %upNumber (Amount Hit Die size is stepped up by)
-   x: %downNumber (Amount Hit Die size is stepped
    down by)
-   x: %Hup (Amount Hit Die size is stepped up by)
-   x: %Hdown (Amount Hit Die size is stepped down by)
-   y: CLASS=&lt;class name&gt; (Optional, Specific
    class the HITDIE will be applied to)
-   y: CLASS.TYPE=&lt;class type name&gt; (Optional,
    Specific class type the HITDIE will be applied to)



What it does
------------

-   Specifies the new Hit Die size granted to the creature by the
    template and retroactively recalculates hit points based on the new
    Hit Die size.
-   The scale used by the functions which raise or lower Hit Die in
    steps is defined by the Game Mode &gt; Misc Info File &gt;
    [DIESIZES](/list/system/gamemode-miscinfo/diesizes.html)
    gameMode tag.
-   The scale used in most gameModes is:
    1,2,3,MIN=4,6,8,10,MAX=12,20,100,1000
-   When using the step up function (%upNumber) or step down function
    (%downNumber), the minimum and maximum steps are set by the `MIN`
    and `MAX` parameters in the `DIESIZES` tag.
-   The step up function (%Hup) and step down functions (%Hdown) will
    ignore the `MIN` and `MAX` settings and use the full range of die
    sizes specified by the `DIESIZES` tag.
-   Regardless of the number specified (x), the new hit die sizw will
    never drop below "1".
-   `HITDIE` can be qualified with a Class or Class type in which case
    it will only be applied to the matching classes.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `HITDIE` tag, the data included in a new `HITDIE`
    tag will overwrite the existing tag data.

Example
-------

`HITDIE:12`

The character now has a Hit Die size of 12.

`HITDIE:%+2`

Adds 2 to the current Hit Die size.

`HITDIE:%-4`

Subtracts 4 from the current Hit Die size.

`HITDIE:%*3`

Multiplies the current Hit Die size by 3.

`HITDIE:%/2`

Divides the current Hit Die size by 2.

`HITDIE:%up2`

Steps up the Hit Die size by two steps. If the creature has a Hit Die of
d6 it will be stepped up to d10.

`HITDIE:%down1`

Steps down the Hit Die size by one step. If the creature has a Hit Die
of d6 it will be stepped down to d4.

`HITDIE:%up1|CLASS.TYPE=Monster`

Steps up the Hit Die size by one step for any Monster class levels the
creature has. If the creature has a Monster class Hit Die of d8 it will
be stepped up to d10.

`HITDIE:%Hup4`

Steps up the Hit Die size by four steps. If the class has a Hit Die of
d6 it will be stepped up to d20.

`HITDIE:%Hdown3`

Steps down the Hit Die size by three steps. If the class has a Hit Die
of d6 it will be stepped down to d2.

`<template name>.MOD <tab> HITDIE:8`

The character now has a Hit Die size of 8.

**.MOD Example:**

Initial Template: `Darkling Sorcerer <tab> HITDIE:6`

Modified By: `Darkling Sorcerer.MOD <tab> HITDIE:8`

Is Equivalent To: `Darkling Sorcerer <tab> HITDIE:8`

The Darkling Sorcerer's Hit Die size is now "8".

