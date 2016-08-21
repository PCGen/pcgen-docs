+++
date = "2016-08-01"
title = "REPEATLEVEL (Data: classes.lst)"
original_url = "list/data/classes.html#repeatlevel"
categories = [ "all-tag", "classes-tag" ]
+++

## Status

None

## Syntax

`w:REPEATLEVEL:x|y|z`

## Parameters

-   w: Number (Class level)
-   w: SUBCLASSLEVEL:Number (Class level)
-   w: SUBSTITUTIONLEVEL:Number (Class level)
-   x: Number (Level interval)
-   y: SKIP=Number (Number of intervals before skipping
    one interval, use 0 for no skip, Optional)
-   z: MAX=Number (Maximum level, Optional)



<span id="repeatlevel"></span> \*\*\* Added 5.13.3

What it does
------------

-   When included, this tag must be the first tag on the line.
-   All the tags included on the line will be applied again at later
    levels at intervals specified by the tag.
-   The progression begins at the level the REPEATLEVEL tag is
    encountered in.
-   Variable x specifies the interval that the line will be repeated, so
    if you specified 3 at level one the line would repeat again at level
    4, 7, 10, etc...
-   Variable y specifies the interval with the first interval where it
    will skip one interval, to continue the above example if you
    specified 3 (variable x) at level one and 2 for variable y the line
    would repeat again at level 4, 10, 13, 19, 22, 28, etc...
-   Variable z specifies the level at which the progression ends.
-   Variables y and z are optional but if you use z you must also use y
    which can be set to 0 if it is not otherwise used.
-   Any valid class tags may be used on the line to be repeated.
-   The REPEATLEVEL tag can be used on the SUBCLASSLEVEL and
    SUBSTITUTIONLEVEL lines.

Example
-------

`5:REPEATLEVEL:5 <tab> ADD:FEAT(ABonusFeat)`

Would add at levels 5,10,15,20,... up to the MAXLEVEL defined by class.

`1:REPEATLEVEL:1|SKIP=4 <tab> ADD:FEAT(ABonusFeat)`

Would add at levels 1,2,3,4,6,7,8,9,11,12,13,14,... up to the MAXLEVEL
defined by class.

`2:REPEATLEVEL:2|SKIP=0|MAX=20 <tab> ADD:FEAT(ABonusFeat)`

Would add at levels 2,4,6,8,... up to level 20.

**Derecated Syntax:**

`5 <tab> REPEATLEVEL:5 <tab> ADD:FEAT(ABonusFeat)`

Where it is used
----------------

Class Level Lines, Sub-class Level Lines, Substitution Level Lines.

