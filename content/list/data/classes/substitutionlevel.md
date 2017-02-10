+++
date = "2016-08-01"
title = "SUBSTITUTIONLEVEL (Data: classes.lst)"
original_url = "/list/data/classes.html#substitutionlevel"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "SUBSTITUTIONLEVEL"
    parent = "data_classes"
+++

## Status

None

## Syntax

`SUBSTITUTIONLEVEL:x`

## Parameters

-   x: Number



<span id="substitutionlevel"></span> \*\*\* Added 5.11.0

What it does
------------

-   Defines a substitution level at which a particular Special Ability
    is granted.
-   This tag MUST be the first tag on a line, and will define a
    substitution level dependent ability for the SUBSTITUTIONCLASS
    immediately above it.
-   Located before the Class Level Lines.

Example
-------

`SUBSTITUTIONLEVEL:4 <tab> SA:Goblin Slave (Ex)`

would add SA:Goblin Slave (Ex) at level 4 instead of the standard level
4 class abilities.

Where it is used
----------------

Substitutionclass Line.

