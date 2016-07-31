+++
date = "2016-08-01"
title = "CASTERLEVEL (Data: classes.lst)"
original_url = "list/data/classes.html#casterlevel"
categories = [ "all-tag", "classes-tag" ]
+++

## Status

None

## Syntax

`BONUS:CASTERLEVEL|x|y`

## Parameters

-   x: Text (Class name)
-   y: Number (Number to add class level)



<span id="casterlevel"></span> \*\*\* Added 5.4

What it does
------------

-   Each spellcasting class should have a CASTERLEVEL bonus associated
    with it.
-   If no CASTERLEVEL bonus is present for a spell casting class, it
    will default to class level.
-   This tag is listed here for this specific use but it is a Global tag
    and has wider uses including raising the caster level of
    racial spells. See the
    [BONUS:CASTERLEVEL](/list/global/bonus/casterlevel.html) entry in
    Global tags for more information.

Example
-------

`BONUS:CASTERLEVEL|Wizard|CL`

Sets the Wizard's spell caster level to his class level.

`BONUS:CASTERLEVEL|Paladin|CL/2|PRECLASSLEVEL:Paladin=4`

Sets the Paladin's spell caster level to half his class level after he
reaches level 4.

Where it is used
----------------

Class Level Line.

