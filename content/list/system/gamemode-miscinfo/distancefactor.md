+++
date = "2016-08-01"
title = "DISTANCEFACTOR (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#distancefactor"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

New 5.9.5

## Syntax

`DISTANCEFACTOR:x`

## Parameters

-   x: Text (Distance factor).



What it does
------------

Used in UNITSET lines to define the distance factor of the unit set.
Distance is multiplied by the unit sets DISTANCEFACTOR and the resulting
conversion is displayed in the GUI. A Unit set which is native to the
data will always have a factor of 1.

Example
-------

`DISTANCEFACTOR:0.3`

Defines the distance factor as "0.3".

Where it is used
----------------

Used in [UNITSET](/list/system/gamemode-miscinfo/unitset.html) lines.

