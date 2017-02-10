+++
date = "2016-08-01"
title = "EQMOD (Data: equipment.lst)"
original_url = "/list/data/equipment.html#eqmod"
categories = [ "all-tag", "equipment-tag" ]
[menu.main]
    name = "EQMOD"
    parent = "data_equipment"
+++

## Status

None

## Syntax

`EQMOD:x|y|y.x|y|y`

## Parameters

-   x: Text (Equipment modifier KEY)
-   y: Text (Variable values)
-   y: Text (Chooser responses)



What it does
------------

-   Applies the included eqmods to an item.
-   The eqmods are a period-delimited (.) list of equipment
    modifier KEYs.
-   Eqmods (x) may include a pipe-delimited (|) list of variable
    values (y) or chooser responses (y) determined by the built-in
    variables or choosers of the eqmod itself. See
    *rsrd\_equipmods\_enhancing.lst* for examples of eqmods.
-   When used in conjunction with `BASEITEM` , the eqmod is
    automatically applied to the base item and is applied before looking
    at other tags.

Example
-------

`EQMOD:KEEN.BANE|Undead`

Creates a sword that is keen and also has Bane Undead.

`EQMOD:ABILITYPLUS|STR+2`

Applies a +2 strength bonus to the character when using the item.

`Leather Armor.MOD <tab> EQMOD:DR_CONVERSION_ARCHAIC|2`

Applies a damage reduction bonus of 2 to the character when using the
item.

> `Rod (Absorption) <TAB> OUTPUTNAME:Rod of [NAME] <TAB> TYPE:Magic.Rod <TAB> COST:50000 <TAB> WT:5 <TAB> BASEITEM:Rod <TAB> EQMOD:CHARGED_ITEM_50|CHARGES[50] <TAB> SOURCEPAGE:MagicItemsIII.rtf`

Creates a magical rod called "Rod of Absorption" with 50 charges.

