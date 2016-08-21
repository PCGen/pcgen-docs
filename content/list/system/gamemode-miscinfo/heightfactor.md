+++
date = "2016-08-01"
title = "HEIGHTFACTOR (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#heightfactor"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

New 5.9.5

## Syntax

`HEIGHTFACTOR:x`

## Parameters

-   x: Number (Height Factor).



What it does
------------

Used in UNITSET lines to define the height factor of the unit set.
Height is multiplied by the unit sets HEIGHTFACTOR and the resulting
conversion is displayed in the GUI. A Unit set which is native to the
data will always have a factor of 1.

Example
-------

`HEIGHTUNIT:2.54`

Defines the height factored as "2.54".

Where it is used
----------------

Used in [UNITSET](/list/system/gamemode-miscinfo/unitset.html) lines.

