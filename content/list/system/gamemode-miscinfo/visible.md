+++
date = "2016-08-01"
title = "VISIBLE (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#visible"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "VISIBLE (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

Updated 5.11.1

## Syntax

`VISIBLE:x`

## Parameters

-   x: YES (Default)
-   x: NO
-   x: QUALIFY



What it does
------------

-   Turns the associated tab or sub-tab on or off in the GUI.
-   `YES` - Used to make the tab display in the GUI.
-   `NO` - Used to keep the tab from displaying in the GUI.
-   `QUALIFY` - Ability category is only displayed if its total pool
    (spent + remaining) is not empty.
-   If the ability category is on its own subtab (see
    [DISPLAYLOCATION](/list/system/gamemode-miscinfo/displaylocation.html) )
    it will always be displayed. As a result it is recommended that
    these optional categories be grouped where possible.

Example
-------

`VISIBLE:NO`

Used to keep the tab from displaying in the GUI.

Where it is used
----------------

Used in [TAB](/list/system/gamemode-miscinfo/tab.html) and
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines.

