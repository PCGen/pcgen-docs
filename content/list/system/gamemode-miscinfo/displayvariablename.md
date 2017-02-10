+++
date = "2016-08-01"
title = "DISPLAYVARIABLENAME (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#displayvariablename"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "DISPLAYVARIABLENAME"
    parent = "system_gamemode-miscinfo"
+++

## Status

None

## Syntax

`DISPLAYVARIABLExNAME:y`

## Parameters

-   x: Number (Variable number, 1, 2, or 3)
-   y: Text (Variable name)



What it does
------------

-   This tag identifies variables to be displayed on the Class Tab.
-   The variable name must match a valid `DEFINE` tag for the variable
    to be displayed.
-   Up to 3 variables can be displayed in this manner.

Example
-------

`DISPLAYVARIABLE1NAME:1`

The ActionRemain variable will be displayed on the Class Tab.

