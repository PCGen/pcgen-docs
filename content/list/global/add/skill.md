+++
date = "2016-08-01"
title = "SKILL (Global: ADD)"
original_url = "/list/global/add.html#skill"
categories = [ "all-tag", "add-tag" ]
[menu.main]
    name = "SKILL"
    parent = "global_add"
+++

## Status

New 5.11.11

## Syntax

`ADD:SKILL|x|y,y`

## Parameters

-   x: Number, Variable or Formula (Number of
    choices granted. Optional)
-   y: Text (Name of skill)



What it does
------------

-   Will add a number (x) of skills from the provided list of skills (y)
    to the character.
-   SKILL with no additional parameters will increase the quantity of
    the items by 1.
-   SKILL with parameters will give the character a choice of one from
    the items listed in the y,y list.
-   SKILL with parameters will give the character a choice up to the
    count parameter from the items listed in the y,y list.
-   The list of skills is a comma-delimited (",") list of skills.

Example
-------

`ADD:SKILL|1|Read/Write Language`

Add one of either a "Read/Write Language".

`ADD:SKILL|5|Balance,Craft (Structural),Demolitions`

Add five skill levels of "Balance" or "Craft (Structural)" or
"Demolitions".

`ADD:SKILL|2|Speak Language`

Add two of "Speak Language".

