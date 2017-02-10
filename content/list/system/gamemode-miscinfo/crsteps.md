+++
date = "2016-08-01"
title = "CRSTEPS (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#crsteps"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "CRSTEPS"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_CRSTEPS"
+++

## Status

New 6.1.2

## Syntax

`CRSTEPS:x|x`

## Parameters

-   x: Text (a fractional CR).



What it does
------------

Lists the "lower than CR 1" CRs in decreasing steps, so that PCGen can
do correct CR reductions and return a string result as used in the
rules.

Example
-------

`CRSTEPS:1/2|1/3|1/4|1/6|1/8`

Descending CR values below CR 1.

