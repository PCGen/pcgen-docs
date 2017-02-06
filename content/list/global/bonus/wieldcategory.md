+++
date = "2016-08-01"
title = "WIELDCATEGORY (Global: BONUS)"
original_url = "/list/global/bonus.html#wieldcategory"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "WIELDCATEGORY (Global: BONUS)"
    parent = "bonus"
+++

## Status

New 5.5.2

## Syntax

`BONUS:WIELDCATEGORY|x,x|y`

## Parameters

-   x: Light (Effects Light weapon category)
-   x: OneHanded (Effects OneHanded weapon category)
-   x: TwoHanded (Effects TwoHanded weapon category)
-   x: ALL (Effects all weapon categories)
-   y: Number, variable or formula (Number to increase
    or decrease the category by)



What it Does
------------

-   Changes the wield category of weapons a character may use.
-   The wield category names are defined in the
    system/gameModes/miscinfo.lst file.
-   This bonus will only have an effect if the gameMode has defined
    wield categories, currently only the 3.5e RSRD gameMode uses
    wield categories.

Example
-------

`BONUS:WIELDCATEGORY|TwoHanded|-1`

Allows a character to wield a larger Two Handed weapon than would
normally be allowed.

`BONUS:WIELDCATEGORY|ALL|-1`

Allows a character to use all weapons that are one Size Category larger.

`BONUS:WIELDCATEGORY|OneHanded,Light|1`

Allows a character to use smaller 'Light' and 'OneHanded' weapons than
would normally be allowed.

