+++
date = "2016-08-01"
title = "DR (Global: OTHER)"
original_url = "/list/global/other.html#dr"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "DR"
    parent = "global_other"
+++

## Status

None

## Syntax

`DR:x/y`

## Parameters

-   x: Number or Formula (Amount of Damage Reduction)
-   y: Text (Damage Type that bypasses this Reduction)



**Prerequisites Allowed:** Yes

What it does
------------

-   This defines the damage reduction this feat/class/template/etc.
    bestows.
-   Multiple damage types can be specified by separating them with "and"
    or "or" as appropriate.
-   DR tags with the same damage types do not stack, only the DR tag
    with the highest value will be used.
-   Damage Reductions must be first defined in this manner before a
    [BONUS:DR](/list/global/bonus/dr.html) tag can be used to add
    to them.
-   If a lst file tries to do a BONUS:DR|+1|10 and no DR:xx/+1 has ever
    been defined, the bonus will do nothing.
-   DR tags can be qualified with [PRExxx](/list/global/pre.html) tags.
    DR tags qualified with PRExxx tags will not display unless the
    character meets the prerequisites.

Example
-------

`DR:10/+1`

Grants DR of 10/+1 on output.

`DR:2/-|PRESTAT:1,CON=18`

Grants DR of 2/- if the character has a constitution of 18 or higher.

