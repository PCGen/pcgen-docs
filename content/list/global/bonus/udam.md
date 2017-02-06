+++
date = "2016-08-01"
title = "UDAM (Global: BONUS)"
original_url = "/list/global/bonus.html#udam"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "UDAM (Global: BONUS)"
    parent = "bonus"
+++

## Status

New 5.5

## Syntax

`BONUS:UDAM|x|y`

## Parameters

-   x: CLASS.Text (Class name)
-   y: Number, variable or formula (Levels to add to
    unarmed damage)



What it Does
------------

This tag adds levels to the character's unarmed damage bonus as if
he/she had gained those levels as a Monk.

Example
-------

`BONUS:UDAM|CLASS.Monk|5`

Unarmed damage is treated as a Monk of five levels higher. For this to
work you must have Monk levels.

`BONUS:UDAM|CLASS.Monk|CL=SpecialMonk`

Would raise the Monk's Unarmed Damage "level" by the Class Level of the
"SpecialMonk" class.

