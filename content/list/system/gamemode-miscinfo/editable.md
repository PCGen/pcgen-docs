+++
date = "2016-08-01"
title = "EDITABLE (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#editable"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "EDITABLE (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

New 5.11.1

## Syntax

`EDITABLE:x`

## Parameters

-   x: Boolean (Yes or No)



What it does
------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines to define whether this category of abilities is user-editable. If
editable, the normal abilities may be added or removed by the user
through the UI.

Example
-------

`EDITABLE:No`

Defines that abilities of this category can not be edited by the user.

Where it is used
----------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines.

