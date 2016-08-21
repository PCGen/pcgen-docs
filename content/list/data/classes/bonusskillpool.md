+++
date = "2016-08-01"
title = "BONUSSKILLPOOL (Data: classes.lst)"
original_url = "list/data/classes.html#bonusskillpool"
categories = [ "all-tag", "classes-tag" ]
+++

## Status

None

## Syntax

`BONUS:SKILLPOOL|NUMBER|x`

## Parameters

-   x: Number, variable or formula (Number to add to
    skill pool)



<span id="bonusskillpool"></span> \*\*\* Added 5.3.9

What it does
------------

-   Adds to the number of skill points to the class at the level that
    the bonus appears in
-   PRExxx tags may be used with this tag.
-   This tag is valid in only class and class level lines.

Examples
--------

`BONUS:SKILLPOOL|NUMBER|1`

Adds one skill point to the skill pool.

`BONUS:SKILLPOOL|NUMBER|1|PREFEAT:1,Scribe Scroll`

Adds one skill point to the skill pool if the character has the Scribe
Scroll Feat.

Where it is used
----------------

Class Line.

