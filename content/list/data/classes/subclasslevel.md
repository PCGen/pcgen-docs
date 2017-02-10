+++
date = "2016-08-01"
title = "SUBCLASSLEVEL (Data: classes.lst)"
original_url = "/list/data/classes.html#subclasslevel"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "SUBCLASSLEVEL"
    parent = "data_classes"
    identifier = "data_classes_SUBCLASSLEVEL"
+++

## Status

None

## Syntax

`SUBCLASSLEVEL:x`

## Parameters

-   x: Number



<span id="subclasslevel"></span> \*\*\* Added 4.3.1

What it does
------------

-   Defines a subclass level at which a particular Special Ability
    is granted.
-   This tag should MUST be the first tag on a line, and will define a
    Subclass level dependent ability for the SUBCLASS immediately
    above it.
-   Located before the Class Level Lines.

Example
-------

`SUBCLASSLEVEL:3 <tab> SA:Angelfire`

would add SA:Angelfire at level 3

Where it is used
----------------

Subclass Line.

