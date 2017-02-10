+++
date = "2016-08-01"
title = "FEAT (Global: ADD)"
original_url = "/list/global/add.html#feat"
categories = [ "all-tag", "add-tag" ]
[menu.main]
    name = "FEAT"
    parent = "global_add"
+++

## Status

New 5.11.11

## Syntax

`ADD:FEAT|x|y,y`

## Parameters

-   x: Number, Variable or Formula (Number of
    choices granted. Optional)
-   y: Text (Feat name)
-   y: ALL (List of all feats.)
-   y: TYPE=Text (Feat type)



What it does
------------

-   Will add a number (x) of feats from the presented list of feats (y).
-   The feat list (y) is a comma-delimited (",") list.
-   Wildcards (%), e.g. Skill Focus(Craft%), can be used in this tag.
-   If the parameter (x) is not used, the count defaults to "1".
-   If the feat being added has a chooser, `ADD:FEAT` will activate it.
    ( `FEAT` alone will not.)

Example
-------

`ADD:FEAT|2|Alertness,TYPE=Fighter,Electric Boogalo`

Add two feats from a list of feats consisting of "Alertness", any
"Fighter" type feats and "Electric Boogalo".

`ADD:FEAT|TYPE=General,TYPE=Metamagic,TYPE=ItemCreation`

Add one feat from the list of feats consisting of "General", any
"Metamagic", or any "ItemCreation" type feats.

`ADD:FEAT|2|ALL`

Add two feats from all feats available.

`ADD:FEAT|Skill Focus(Craft%)`

Add the skill focus feat and choose only from the Skills with the name
that begins with 'Craft'.

