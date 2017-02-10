+++
date = "2016-08-01"
title = "SIZEDIFF (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#sizediff"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "SIZEDIFF"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 5.5.2

## Syntax

`SIZEDIFF:x`

## Parameters

-   x: Number (effective object size difference)



What it does
------------

Defines the effective object size difference from the base Weapon size.

This is used for the Object Size computations within the java code.

Example
-------

`SIZEDIFF:-1`

If this weapon was Medium sized, then this weapon would have a Small
object size.

Where it is used
----------------

After a WIELDCATEGORY tag.

