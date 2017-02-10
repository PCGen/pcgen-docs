+++
date = "2016-08-01"
title = "LANGBONUS (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#langbonus"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "LANGBONUS"
    parent = "data_startingkits"
    identifier = "data_startingkits_LANGBONUS"
+++

## Status

New 5.15.4

## Syntax

`LANGBONUS:x|x`

## Parameters

-   x: Text (Language)



What it does
------------

-   `LANGBONUS` chooses from the Bonus Language Selections if there are
    enough language bonuses to be spent.
-   This tag requires that a `LANGBONUS` tag be included in the <span
    class="lstfile">race.lst</span> file in which the character upon
    which the kit is being applied to is defined.

Where it is used
----------------

LANGBONUS is used in kit lines.

Example
-------

`LANGBONUS:Dwarven|Elvish`

Selects Dwarven and Elvish langauges.

