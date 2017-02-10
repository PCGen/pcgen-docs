+++
date = "2016-08-01"
title = "UNITSET (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#unitset"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "UNITSET"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_UNITSET"
+++

## Status

New 5.9.5

## Syntax

`UNITSET:x`

## Parameters

-   x: Text (Name of the Unit Set).



What it does
------------

UNITSET begins a line which defines a system of measurements such as
Imperial or Metric. Unit sets can be selected on the language tab of the
preferences dialog, by name. The Unit set in which the data is native
should always have a factor of 1. The Default Unit Set is set in the
miscinfo.lst file with the
[DEFAULTUNITSET](/list/system/gamemode-miscinfo/defaultunitset.html) tag
and will default to Imperial if not present.

**Tags used in UNITSET lines:**

[DISTANCEUNIT](/list/system/gamemode-miscinfo/distanceunit.html)

[DISTANCEFACTOR](/list/system/gamemode-miscinfo/distancefactor.html)

[DISTANCEPATTERN](/list/system/gamemode-miscinfo/distancepattern.html)

[HEIGHTUNIT](/list/system/gamemode-miscinfo/heightunit.html)

[HEIGHTFACTOR](/list/system/gamemode-miscinfo/heightfactor.html)

[HEIGHTPATTERN](/list/system/gamemode-miscinfo/heightpattern.html)

[WEIGHTUNIT](/list/system/gamemode-miscinfo/weightunit.html)

[WEIGHTFACTOR](/list/system/gamemode-miscinfo/weightfactor.html)

[WEIGHTPATTERN](/list/system/gamemode-miscinfo/weightpattern.html)

Example
-------

`UNITSET:Imperial`

Defines a Unit Set named Imperial.

