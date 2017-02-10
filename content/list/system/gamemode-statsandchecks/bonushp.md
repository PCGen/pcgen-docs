+++
date = "2016-08-01"
title = "BONUSHP (Game Mode: statsandchecks.lst)"
original_url = "/list/system/gamemode-statsandchecks.html#bonushp"
categories = [ "all-tag", "gamemode-statsandchecks-tag" ]
[menu.main]
    name = "BONUSHP"
    parent = "system_gamemode-statsandchecks"
    identifier = "system_gamemode-statsandchecks_BONUSHP"
+++

## Status

None

## Syntax

`BONUS:HP|x|y`

## Parameters

-   x: Text (A defined HP type).
-   y: Formula (Amount to add to the HP type).



What it does
------------

Sets a bonus to the HP type specified.

Example
-------

`BONUS:HP|WOUNDPOINTS|CON`

Adds a characters CON bonus to the WOUNDPOINTS total at each level.

`BONUS:HP|ALTHP|CONSCORE`

Adds a characters CONSCORE to the ALTHP total as defined in
miscinfo.lst.

`BONUS:HP|BONUS|CON`

Adds a characters CON bonus to the Primary HP total as defined in
miscinfo.lst.

`BONUS:HP|CON`

Adds a characters CON bonus to the Primary HP total as defined in
miscinfo.lst.

Where it is used
----------------

STATNAME Line.

