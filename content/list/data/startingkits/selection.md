+++
date = "2016-08-01"
title = "SELECTION (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#selection"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "SELECTION"
    parent = "data_startingkits"
    identifier = "data_startingkits_SELECTION"
+++

## Status

New 5.15.4

## Syntax

`SELECTION:x,x`

## Parameters

-   x: Text (Language)



What it does
------------

-   Makes selection of languages for ranks of the Speak Language skill.
-   This tag is used, in conjunction with the `SKILL` and `RANK` tags,
    to select languages.

Example
-------

`SKILL:Speak Language <tab> RANK:2 <tab> SELECTION:Dwarven,Elven`

Selects Dwarven and Elven languages with the ranks bought.

Where it is used
----------------

SKILL lines

