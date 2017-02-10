+++
date = "2016-08-01"
title = "ABILITY (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#ability"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "ABILITY"
    parent = "data_startingkits"
    identifier = "data_startingkits_ABILITY"
+++

## Status

New 5.9.7

## Syntax

`ABILITY:PROMPT:FEAT(x)|CHOICE:y`

## Parameters

-   x: Text (Feat choices)
-   y: Text (Feat to select)



What it does
------------

The `ABILITY` tag is used to select the choice presented by an
`ADD:FEAT` chooser in a class level line.  The Feat choices parameter
must match the choices used in the `ADD:FEAT` this `ABILITY` is
selecting for.  The Feat to select should be a valid selection but this
is not checked by the kit.

Example
-------

`LEVELABILITY:Ranger=1 <tab> ABILITY:PROMPT:FEAT(TYPE.Favored Enemy)|CHOICE:Favored Enemy (Humanoid (Elf))`

Selects Humanoid (Elf) as a ranger's first favored enemy selection.

Where it is used
----------------

LEVELABILITY line

