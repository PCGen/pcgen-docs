+++
date = "2016-08-01"
title = "PRESTAT (Global: PRErequisite)"
original_url = "/list/global/pre.html#prestat"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRESTAT (Global: PRErequisite)"
    parent = "pre"
+++

## Status

None

## Syntax

`PRESTAT:x,y=z,y=z`

## Parameters

-   x: Number (The number of stats that must match).
-   y: Text (The stats abbreviation - as defined
    in statsandchecks.lst).
-   z: Number (The minimum value of the stat).



What it does
------------

Sets stat requirements.

Examples
--------

`PRESTAT:1,STR=18`

Character must have an 18 Strength to meet the requirement.

`PRESTAT:1,STR=18,WIS=18`

Either STR or WIS at 18 - one of the two listed must meet the
requirements.

`PRESTAT:2,STR=18,WIS=18`

BOTH STR and WIS at 18 - two of the two listed must meet the
requirements.

`PRESTAT:1,STR=15,WIS=13`

Either STR at 15 or WIS at 13 - one of the two listed must meet the
requirements.

`PRESTAT:2,STR=13,INT=10,CHA=13`

Either STR at 13, INT at 10 or CHA at 13 - two of the three listed must
meet the requirements.

