+++
date = "2016-08-01"
title = "WEIGHTFACTOR (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#weightfactor"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "WEIGHTFACTOR"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_WEIGHTFACTOR"
+++

## Status

New 5.9.5

## Syntax

`WEIGHTFACTOR:x`

## Parameters

-   x: Text (Weight factor).



What it does
------------

Used in UNITSET lines to define the weight factor of the unit set.
Weight is multiplied by the unit sets WEIGHTFACTOR and the resulting
conversion is displayed in the GUI. A Unit set which is native to the
data will always have a factor of 1.

Example
-------

`WEIGHTFACTOR:0.5`

Defines the weight factor as "0.5".

Where it is used
----------------

Used in [UNITSET](/list/system/gamemode-miscinfo/unitset.html) lines.

