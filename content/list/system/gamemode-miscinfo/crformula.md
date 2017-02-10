+++
date = "2016-08-01"
title = "CRFORMULA (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#crformula"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "CRFORMULA"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_CRFORMULA"
+++

## Status

Updated 6.1.2

## Syntax

`CRFORMULA:x`

## Parameters

-   x: Formula (a standard PCGen LST formula).



What it does
------------

Specifies the formula to be used when calculating the CR, or "NONE" to
define a class type for creatures that do not have a CR value, such als
animal companions.

Example
-------

`CRFORMULA:CL`

CR for a class of this type is equal to CL (Class Level).

Where it is used
----------------

CLASSTYPE Line.

