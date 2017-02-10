+++
date = "2016-08-01"
title = "MAXDEVVER (Game Mode: migration.lst)"
original_url = "/list/system/gamemode-migration.html#maxdevver"
categories = [ "all-tag", "gamemode-migration-tag" ]
[menu.main]
    name = "MAXDEVVER"
    parent = "system_gamemode-migration"
+++

## Status

New 6.01.03

## Syntax

`MAXDEVVER:x`

## Parameters

-   x: Text (Version number)



What it does
------------

-   Specifies the developmental version of PCGen (e.g. alpha, beta) when
    the associated lst object was last coded in the old format.
-   This tag is optional and if included must be later than `MAXVER` .

Example
-------

`MAXDEVVER:6.01.07`

The associated lst object was coded for PCGen developmental version
6.01.07 or earlier.

