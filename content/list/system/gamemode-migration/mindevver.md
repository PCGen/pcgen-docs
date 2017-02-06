+++
date = "2016-08-01"
title = "MINDEVVER (Game Mode: migration.lst)"
original_url = "/list/system/gamemode-migration.html#mindevver"
categories = [ "all-tag", "gamemode-migration-tag" ]
[menu.main]
    name = "MINDEVVER (Game Mode: migration.lst)"
    parent = "gamemode-migration"
+++

## Status

New 6.01.03

## Syntax

`MINDEVVER:x`

## Parameters

-   x: Text (Version number)



What it does
------------

-   Specifies the developmental version of PCGen (e.g. alpha, beta) when
    the associated lst object was first coded in the old format.
-   This tag is optional and if included must be later than `MINVER` .

Example
-------

`MINDEVVER:6.01.01`

The associated lst object was coded for PCGen developmental version
6.01.01 or later.

