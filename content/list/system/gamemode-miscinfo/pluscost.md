+++
date = "2016-08-01"
title = "PLUSCOST (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#pluscost"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "PLUSCOST (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

None

## Syntax

`PLUSCOST:x`

## Parameters




**Variables used (x):** formula

What it does
------------

Defines base item costs and modifier costs based upon the formula
entered.

Example
-------

`PLUSCOST:AMMUNITION|BASEQTY*40*PLUS*PLUS`

Ammunition will be based upon quantity times 40 times the plus value
desired and times the plus value desired again to result in the final
cost.

`PLUSCOST:ARMOR|1000*PLUS*PLUS`

Takes the armor cost and then takes 1000 times the plus value and then
times the plus value to come up with the resulting cost.

`PLUSCOST:SHIELD|1000*PLUS*PLUS`

Takes the shield cost and then takes 1000 times the plus value and then
times the plus value to come up with the resulting cost.

`PLUSCOST:WEAPON|(2000*PLUS*PLUS)+(2000*ALTPLUS*ALTPLUS)`

Takes the weapon cost and then takes 2000 times the plus value and then
times the plus value to come up with the resulting cost, if the weapon
has an alternate head (double weapon) it also calculates the cost using
the same formula.

