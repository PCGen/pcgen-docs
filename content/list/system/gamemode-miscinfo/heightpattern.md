+++
date = "2016-08-01"
title = "HEIGHTPATTERN (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#heightpattern"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "HEIGHTPATTERN (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

New 5.9.5

## Syntax

`HEIGHTPATTERN:x`

## Parameters

-   x: Text (Distance unit pattern).



What it does
------------

Used in UNITSET lines to define the distance unit pattern of the unit
set. The 'pattern' string is a pattern for formatting the output of the
value, so you can specify e.g. how many decimal digits are printed. The
pattern follows the definition of the Java class DecimaFormat and can be
found
[here](http://java.sun.com/j2se/1.3/docs/api/java/text/DecimalFormat.html)
.

Example
-------

`HEIGHTPATTERN:#`

Defines the distance unit pattern as "\#".

Where it is used
----------------

Used in [UNITSET](/list/system/gamemode-miscinfo/unitset.html) lines.

