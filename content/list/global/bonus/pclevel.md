+++
date = "2016-08-01"
title = "PCLEVEL (Global: BONUS)"
original_url = "/list/global/bonus.html#pclevel"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "PCLEVEL"
    parent = "global_bonus"
+++

## Status

None

## Syntax

`BONUS:PCLEVEL|x|y`

## Parameters

-   x: Text (Class name)
-   x: TYPE.Text (Class or Spell type)
-   y: Number, variable or formula (Bonus value)



What it Does
------------

-   Increases the spellcasting level Class, class type, or spell
    type identified.
-   The character must already have a level in a spellcasting class to
    gain the bonus spellcasting level.
-   The syntax `BONUS:PCLEVEL|TYPE=x|y` is valid but in the context of
    this tag it is converted to `BONUS:PCLEVEL|TYPE.x|y` by PCGen on
    the fly.

Examples
--------

`BONUS:PCLEVEL|Sorcerer|1`

Adds 1 to Sorcerer spell caster level.

`BONUS:PCLEVEL|TYPE.Arcane|1`

Adds 1 to Arcane spell caster level.

