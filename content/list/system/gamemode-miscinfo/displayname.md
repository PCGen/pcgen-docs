+++
date = "2016-08-01"
title = "DISPLAYNAME (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#displayname"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "DISPLAYNAME"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_DISPLAYNAME"
+++

## Status

New 5.11.1

## Syntax

`DISPLAYNAME:x`

## Parameters

-   x: Text (The name or key to the name)



What it does
------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines to define the displayed name for this category. If this tag is set
to in\_name (ie: in\_feat) it will pull the name from the language files
(for internationalization).

Example
-------

`DISPLAYNAME:in_feat`

The displayed name for the category is the value in the selected
language for the key in\_feat.

Where it is used
----------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines.

