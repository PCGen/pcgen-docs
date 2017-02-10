+++
date = "2016-08-01"
title = "CLASSSKILLS (Data: classes.lst)"
original_url = "/list/data/classes.html#classskills"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "CLASSSKILLS"
    parent = "data_classes"
+++

## Status

None

## Syntax

`ADD:CLASSSKILLS|x|y,y`

## Parameters

-   x: Number, Variable or Formula (Number of
    choices granted. Optional)
-   y: Text (Name of skill)
-   y: TYPE=Text (Type of skill)
-   y: ALL
-   y: ANY
-   y: CROSSCLASSSKILLS
-   y: UNTRAINED
-   y: TRAINED
-   y: EXCLUSIVE
-   y: NONEXCLUSIVE
-   y: AUTORANK=Number (Number of ranks)



<span id="classskills"></span> \*\*\* Added 5.11.11

What it does
------------

-   Adds a number (x) of skills selected from the presented list (y) to
    the character's class skills list.
-   If a number (x) of choices allowed is not included, "1" is assumed.
-   The skills list (y) is a comma-delimited (",") list of skills.
-   If `ANY` or `ALL` are used, the list of skills to select from will
    include all skills.
-   If `CROSSCLASSSKILLS` is used, the list of skills to select from
    will include all cross-class skills.
-   If `UNTRAINED` is used, the list of skills to select from will
    include all untrained skills.
-   If `TRAINED` is used, the list of skills to select from will include
    all trained skills.
-   If `EXCLUSIVE` is used, the list of skills to select from will
    include all skills exclusive to the associated class.
-   If `NONEXCLUSIVE` is used, the list of skills to select from will
    include all skills that are not exclusive to the assiciated class.
-   AUTORANK will assign free ranks to any chosen skills.

Example
-------

`ADD:CLASSSKILLS|Knowledge (Reverie)`

Add "Knowledge (Reverie)" skill to the character's list of class skills.

`ADD:CLASSSKILLS|Knowledge (nature),Survival,AUTORANK=3`

Add "Knowledge (nature)" and "Survival" skills to the character's list
of class skills and grant 2 free ranks in each.

`ADD:CLASSSKILLS|TYPE=Craft`

Add one skill from the list of "Craft" type skills to the character's
list of class skills.

`ADD:CLASSSKILLS|3|ANY`

Add three skills from the full list of skills to the character's list of
class skills.

`ADD:CLASSSKILLS|3|ALL`

Add three skills from the full list of skills to the character's list of
class skills.

`ADD:CLASSSKILLS|CROSSCLASSSKILLS`

Add one skill from the list of cross-class skills to the character's
list of class skills.

`ADD:CLASSSKILLS|UNTRAINED`

Add one skill from the list of skills that can be used untrained to the
character's list of class skills.

`ADD:CLASSSKILLS|3|TRAINED`

Add three skills from the list of skills that require training to the
character's list of class skills.

`ADD:CLASSSKILLS|2|EXCLUSIVE`

Add two skills from the list of exclusive skills to the character's list
of class skills.

`ADD:CLASSSKILLS|2|NONEXCLUSIVE`

Add two skills from the list of non-exclusive skills to the character's
list of class skills.

