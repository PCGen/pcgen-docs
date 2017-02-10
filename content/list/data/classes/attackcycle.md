+++
date = "2016-08-01"
title = "ATTACKCYCLE (Data: classes.lst)"
original_url = "/list/data/classes.html#attackcycle"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "ATTACKCYCLE"
    parent = "data_classes"
+++

## Status

None

## Syntax

`ATTACKCYCLE:x`

## Parameters

-   x: BAB, RAB, or UAB



<span id="attackcycle"></span> \*\*\* Updated 5.11.6

What it does
------------

-   This sets the Melee/Grapple (BAB - yes, misleading), Ranged (RAB),
    or Unarmed Attack (UAB) cycles.
-   Default is 5 for all.
-   Once a Cycle is reached, the character gets another attack (+6/+1 is
    one 5 cycle.)

Example
-------

`ATTACKCYCLE:UAB|3`

Grants another attack ever 3 bonus points of BAB from the class to the
Unarmed attack cycle.

Where it is used
----------------

Class Line.

