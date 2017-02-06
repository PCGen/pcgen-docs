+++
date = "2016-08-01"
title = "TEMPLATE (Global: ADD)"
original_url = "/list/global/add.html#template"
categories = [ "all-tag", "add-tag" ]
[menu.main]
    name = "TEMPLATE (Global: ADD)"
    parent = "add"
+++

## Status

New 5.11.11

## Syntax

`ADD:TEMPLATE|x|y,y`

## Parameters

-   x: Number, Variable or Formula (Number of
    choices granted. Optional)
-   y: Text (Name of template)



What it does
------------

-   Will add a number (x) of templates from the provided list (y) to
    the character.
-   If the count (x) is not used, "1" is assumed.
-   The template list (y) is a comma-delimited (",") list.

Example
-------

`ADD:TEMPLATE|1|Scholar,Soldier`

Add one of either a "Scholar" or a "Soldier".

`ADD:TEMPLATE|Robot`

Add one of "Robot".

`ADD:TEMPLATE|2|Suite of St. Daris,Suite of St. Feldin,Suite of Lothian`

Add two of "Suite of St. Daris", "Suite of St. Feldin" or "Suite of
Lothian".

