+++
date = "2016-08-01"
title = "VFEAT (Global: ADD)"
original_url = "/list/global/add.html#vfeat"
categories = [ "all-tag", "add-tag" ]
[menu.main]
    name = "VFEAT (Global: ADD)"
    parent = "add"
+++

## Status

New 5.11.11

## Syntax

`ADD:VFEAT|x|y,y`

## Parameters

-   x: Number, Variable or Formula (Number of
    choices granted. Optional)
-   y: Text (Feat name)
-   y: TYPE=Text (Type of feat)
-   y: ALL



What it does
------------

-   Will add a number (x) of virtual feats from the provided list of
    feats (y) to the character regardless of qualification.
-   Feats listed are a comma-delimited "," list.
-   If the parameter (x) is not used, the count defaults to "1".
-   If the feat being added has a chooser, `ADD:VFEAT` will activate it.
    ( `VFEAT` alone will not.)
-   Once added, virtual feats cannot be removed.

Example
-------

`ADD:VFEAT|Weapon Master(TYPE=Weapon)`

Add Weapon Master feat, for any "Weapon" type, as a virtual feat.

`ADD:VFEAT|TYPE=General,TYPE=Metamagic,TYPE=ItemCreation`

Add one virtual feat from types "General", "Metamagic", and
"ItemCreation" type feats.

`ADD:VFEAT|2|ALL`

Add two virtual feats selected from among all feats.

