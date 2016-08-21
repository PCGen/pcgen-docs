+++
date = "2016-08-01"
title = "DISTANCEPATTERN (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#distancepattern"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

New 5.9.5

## Syntax

`DISTANCEPATTERN:x`

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

`DISTANCEPATTERN:#`

Defines the distance unit abbreviation as "\#".

Where it is used
----------------

Used in [UNITSET](/list/system/gamemode-miscinfo/unitset.html) lines.

