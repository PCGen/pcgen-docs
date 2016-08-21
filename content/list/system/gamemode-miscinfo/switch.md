+++
date = "2016-08-01"
title = "SWITCH (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#switch"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

New 5.5.2

## Syntax

`SWITCH:x`

## Parameters

-   x: Text (new name)



What it does
------------

The new name is one of the defined WIELDCATEGORY names.

This is coupled with a PREVARxx:formula to figure the effective wield
category of a weapon based on PC size. Standard PRExxx formulas used to
compute size difference between weapon and PC. If the PREVARxxx formula
is true, then the SWITCH type is applied. This allows changes in
effective wield category based on weapon and PC size.

Example
-------

`SWITCH:Light`

Wield category is switched to 'Light'.

Where it is used
----------------

After a WIELDCATEGORY tag with a PREVARxx statement in it.

