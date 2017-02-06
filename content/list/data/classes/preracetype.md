+++
date = "2016-08-01"
title = "PRERACETYPE (Data: classes.lst)"
original_url = "/list/data/classes.html#preracetype"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "PRERACETYPE (Data: classes.lst)"
    parent = "classes"
+++

## Status

None

## Syntax

`PRERACETYPE:x`

## Parameters

-   x: Text (Race Type)



<span id="preracetype"></span> \*\*\* Updated 5.9.4

What it does
------------

-   This tag checks both the `TYPE` and `RACETYPE` tags in the original
    race file entry, ignoring any race types aquired outside of the
    original race file entry.
-   For monster classes the race must be of this type or they can not
    take the class.

Where it is used
----------------

Class Line.

Example
-------

`PRERACETYPE:Animal`

This class can only be taken by "Animal" races.

