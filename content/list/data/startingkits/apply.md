+++
date = "2016-08-01"
title = "APPLY (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#apply"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "APPLY"
    parent = "data_startingkits"
    identifier = "data_startingkits_APPLY"
+++

## Status

New 5.9.6

## Syntax

`APPLY:x`

## Parameters

-   x: Text (INSTANT or PERMANENT)



What it does
------------

Selects if the selection of this kit is stored with the character or
not.

-   PERMANENT - means the kit will be stored with the character that
    selects it and will not be available to be selected again. (This is
    the default setting.)
-   INSTANT - means the kit will not be stored and can be selected any
    number of times.

Examples
--------

`APPLY:INSTANT`

Sets this kit to be usable multiple times.

Where it is used
----------------

STARTPACK line

