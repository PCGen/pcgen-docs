+++
date = "2016-08-01"
title = "TYPE (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#type"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

New 5.11.1

## Syntax

`TYPE:x.x`

## Parameters

-   x: Text (An ability type).
-   x: \* (Special Wildcard)



What it does
------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines to define the list of types included in this category. Any ability
of any of the specified types will be returned when querying for the
abilities in the category.

Where it is used
----------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines.

Example
-------

`TYPE:Fighter.Wizard`

Defines that all fighter and wizard abilities should be included in the
category.

`TYPE:*`

Defines that all abilities should be included in the category.



