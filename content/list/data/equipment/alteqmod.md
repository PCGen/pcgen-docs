+++
date = "2016-08-01"
title = "ALTEQMOD (Data: equipment.lst)"
original_url = "/list/data/equipment.html#alteqmod"
categories = [ "all-tag", "equipment-tag" ]
[menu.main]
    name = "ALTEQMOD"
    parent = "data_equipment"
+++

## Status

None

## Syntax

`ALTEQMOD:x|y|y.x|y|y`

## Parameters

-   x: Text, period delimited (Equipment modifier name)
-   y: Text, pipe delimited (Modifiers applied to the
    equipment modifier name)



<span id="alteqmod"></span> \*\*\* Added 5.7.15

What it does
------------

-   This is a period (.) delimited list of equipment modifiers applied
    to the secondary head of a double weapon.
-   With the exception that it is applied to the secondary head is
    functions in the same way as the
    [EQMOD](/list/data/equipment/eqmod.html) tag.
-   This is utilized by other EQMODs which contain the ASSIGNTOALL tag.
    For example the Darkwood EQMOD has ASSIGNTOALL:YES and it replaces
    wood, for this to work correctly a double weapon needs to have both
    the EQMOD:WOOD and ALTEQMOD:WOOD tags present. When they are present
    the Darkwood EQMOD is applied to and replaces the WOOD EQMOD on
    both heads.

Example
-------

`ALTEQMOD:WOOD`

2nd head has the WOOD EQMOD applied to it.

