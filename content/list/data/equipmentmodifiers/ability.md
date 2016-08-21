+++
date = "2016-08-01"
title = "ABILITY (Data: equipment_modifiers.lst)"
original_url = "list/data/equipmentmodifiers.html#ability"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
+++

## Status

None

## Syntax

`CHOOSE:ABILITY|x|y,y`

## Parameters

-   x: Text (Ability category)
-   y: Text (Ability name)
-   y: TYPE=Text (Ability type)



<span id="ability"></span> \*\*\* New 5.13.9

What it does
------------

-   Will present a list of abilities, by name and/or type, of the
    specified category.
-   At least one ability or ability type must be designated for this tag
    to function properly.

Example
-------

`CHOOSE:ABILITY|FEAT|TYPE=Rogue Abilities`

A list of all "Rogue Abilities" type feats will be presented.

