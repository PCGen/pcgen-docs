+++
date = "2016-08-01"
title = "PREWIELD (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#prewield"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "PREWIELD (Data: equipment_modifiers.lst)"
    parent = "equipmentmodifiers"
+++

## Status

None

## Syntax

`PREWIELD:x,y,y`

## Parameters

-   x: Number (The number of the wield categories that
    must match)
-   y: Text (Light, OneHanded or TwoHanded)



What it does
------------

-   Makes specific wield categories prerequisites. (See
    [WIELD](/list/data/equipment/wield.html) ).
-   Wield categories are defined in the
    [miscinfo.lst](/list/system/gamemode-miscinfo.html) gamemode file by
    the
    [WIELDCATEGORY](/list/system/gamemode-miscinfo/wieldcategory.html) tag.

Example
-------

`PREWIELD:1,Light,OneHanded`

Weapon must be either Light or OneHanded.

`PREWIELD:1,TwoHanded`

Weapon must be TwoHanded.

