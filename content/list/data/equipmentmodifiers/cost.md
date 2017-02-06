+++
date = "2016-08-01"
title = "COST (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#cost"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "COST (Data: equipment_modifiers.lst)"
    parent = "equipmentmodifiers"
+++

## Status

None

## Syntax

`COST:x`

## Parameters

-   x: Number (Cost or Formula)



What it does
------------

-   The cost applied to the item after resizing it.
-   Formulas can be used with this tag, and valid variables for the
    formulas are:
    -   ALTPLUSTOTAL - The total plus (+) for the second head on a
        double weapon. Will return zero (0) if there is no second head.
    -   BASECOST - The unmodified cast value of the equipment.
    -   CRITMULT - The critical multiplier of the weapon.
    -   DMGDICE - The damage dice of the weapon.
    -   DMGDIE - The damage die of the weapon.
    -   HEADPLUSTOTAL - The total plus (+) for the head the equipmod is
        applied to.
    -   PLUSTOTAL - The total plus (+) for the primary head, for
        weapons, or main object, for non weapons.
    -   RANGE - The range of the weapon.
    -   SIZE - The size of the equipment.
    -   WT - The weight of the equipment.
    -   %CASTERLEVEL - The caster level of the spell being added by
        the modifier.
    -   %CHARGES - The number of charges being added by the modifier.
    -   %SPELLCOST - The spell cost of the spell being added by
        the modifier.
    -   %SPELLLEVEL - The spell level of the spell being added by
        the modifier.
    -   %SPELLXPCOST - The experience point cost of the spell being
        added by the modifier.

Example
-------

`COST:300`

Adds 300 gold to the equipments cost.

`COST:BASECOST/2`

Adds half the base cost of the equipment to the cost.

`COST:500*WT`

Adds 500 gold per lb. to the equipments cost.

`COST:((BASECOST/50)*%CHARGES)-BASECOST`

Assuming this modifier adds 50 charges to the item, this formula makes
the value of a charge one fiftieth of the basecost making the cost of
the equipment proportional to the number of charges left in it.

`COST:(25*((%SPELLLEVEL)MAX(1/2))*%CASTERLEVEL)+%SPELLCOST+(5*%SPELLXPCOST)`

This is the cost formula from a scroll EQMOD.

