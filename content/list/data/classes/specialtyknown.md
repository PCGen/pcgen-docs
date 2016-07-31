+++
date = "2016-08-01"
title = "SPECIALTYKNOWN (Data: classes.lst)"
original_url = "list/data/classes.html#specialtyknown"
categories = [ "all-tag", "classes-tag" ]
+++

## Status

None

## Syntax

`SPECIALTYKNOWN:x,x,x,x,...`

## Parameters

-   x: Number



<span id="specialtyknown"></span> \*\*\* Updated 5.11.4

What it does
------------

Adds the numeric value given to the number of specialty school spells
that the class can cast per spell level. If not listed, the default
value is 0.

Example
-------

`19 <tab> SPECIALTYKNOWN:1,1,1,1,1,1,1,1,1,1`

At 19 level the specialist can prepare one additional Zero thru ninth
level spell (of the school selected as a specialty) per spell level each
day.

`12 <tab> SPECIALTYKNOWN:1,1,1`

At 12 level the Paladin can prepare one third level spell per spell
level each day, he already had a first and second.

Where it is used
----------------

Class Level Line.

