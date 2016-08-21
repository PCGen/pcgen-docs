+++
date = "2016-08-01"
title = "LEVELABILITY (Data: starting_kits.lst)"
original_url = "list/data/startingkits.html#levelability"
categories = [ "all-tag", "startingkits-tag" ]
+++

## Status

New 5.9.7

## Syntax

`LEVELABILITY:x=y`

## Parameters

-   x: Text (Class name)
-   y: Number (Level ability is granted at)



What it does
------------

LEVELABILITY signifies what class and level the following ABILITY tag is
specifying the choice for.

Where it is used
----------------

LEVELABILITY is used in kit lines.

Example
-------

`LEVELABILITY:Ranger=1 <tab> ABILITY:PROMPT:FEAT(TYPE.Favored Enemy)|CHOICE:Favored Enemy (Humanoid (Elf))`

Selects Humanoid (Elf) as a ranger's first favored enemy selection.

