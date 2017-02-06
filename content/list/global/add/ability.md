+++
date = "2016-08-01"
title = "ABILITY (Global: ADD)"
original_url = "/list/global/add.html#ability"
categories = [ "all-tag", "add-tag" ]
[menu.main]
    name = "ABILITY (Global: ADD)"
    parent = "add"
+++

## Status

New 5.11.11

## Syntax

`ADD:ABILITY|w|x|y|z,z..`

## Parameters

-   w: Number, Variable or Formula (Number of
    choices granted. Optional)
-   x: Text (Ability category to which this ability
    will be added.)
-   y: Text (Nature of the added ability)
-   z: Text (Ability name or KEY)
-   z: TYPE=Text (Ability type)



What it does
------------

-   Will add a number (w) of abilities from the presented list (z) and
    will assign it a category (x) and nature (y).
-   The ability list is a comma-delimited (",") list of ability names
    and/or types.
-   Valid ability natures are `NORMAL` or `VIRTUAL` .
-   If the ability being added has a chooser `ADD:ABILITY` is the only
    tag which will activate it ( `ABILITY` alone will not).

Example
-------

`ADD:ABILITY|2|FEAT|NORMAL|Alertness,TYPE=Fighter,Electric Boogalo`

Add two feats from "Alertness", any "Fighter" type feats or "Electric
Boogalo".

`ADD:ABILITY|FEAT|VIRTUAL|TYPE=General,TYPE=Metamagic,TYPE=ItemCreation`

Add one virtual feat from "General", any "Metamagic", any "ItemCreation"
type feats.

