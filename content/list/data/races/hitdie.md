+++
date = "2016-08-01"
title = "HITDIE (Data: races.lst)"
original_url = "list/data/races.html#hitdie"
categories = [ "all-tag", "races-tag" ]
+++

## Status

None

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



<span id="hitdie"></span> \*\*\* Updated 5.13.6

What it does
------------

-   Specifies the new Hit Die size granted to the creature.
-   HITDIE may also be used in [Class](/list/data/classes/hitdie.html)
    and [Template](/list/data/templates/hitdie.html) files.
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
-   Optionally HITDIE can be qualified with a Class or Class type in
    which case it will only be applied to matching classes.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `HITDIE` tag, the data included in a new `HITDIE` tag
    will overwrite the existing tag data.

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

Steps up the Hit Dice size by two steps. If the creature has a Hit Die
of d6 it will be stepped up to d10.

`HITDIE:%down1`

Steps down the Hit Dice size by one step. If the creature has a Hit Die
of d6 it will be stepped down to d4.

`HITDIE:%up1|CLASS.TYPE=Monster`

Steps up the Hit Dice size by one step for any Monster class levels the
creature has. If the creature has a Monster class Hit Die of d8 it will
be stepped up to d10.

`HITDIE:%Hup4`

Steps up the Hit Dice size by four steps. If the class has a Hit Die of
d6 it will be stepped up to d20.

`HITDIE:%Hdown3`

Steps down the Hit Dice size by three steps. If the class has a Hit Die
of d6 it will be stepped down to d2.

**.MOD Example:**

Initial Race: `<race name> <tab> HITDIE:12`

Modified By: `<race name>.MOD <tab> HITDIE:%/2`

Is Equivalent To: `<race name> <tab> HITDIE:%/2`

The creature's new hitdie size is a divided by 2.

