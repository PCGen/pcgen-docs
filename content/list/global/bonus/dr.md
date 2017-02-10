+++
date = "2016-08-01"
title = "DR (Global: BONUS)"
original_url = "/list/global/bonus.html#dr"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "DR"
    parent = "global_bonus"
    identifier = "global_bonus_DR"
+++

## Status

None

## Syntax

`BONUS:DR|x|y`

## Parameters

-   x: Text (Damage reduction type)
-   y: Number, variable or formula (Damage
    reduction amount)



What it Does
------------

Adds a bonus to a Damage Reduction type, previously defined by a
standard [DR](/list/global/other/dr.html) tag (the BONUS tag needs to be
coordinated with a DR:\#/&lt;string&gt;).

Example
-------

`BONUS:DR|+1|10`

If the +1 DR type was currently at 5/+1 this tag would add 10 making it
15/+1.

