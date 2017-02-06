+++
date = "2016-08-01"
title = "CHOOSEEQUIPMENT (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#chooseequipment"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "CHOOSEEQUIPMENT (Data: equipment_modifiers.lst)"
    parent = "equipmentmodifiers"
+++

## Status

None

## Syntax

`CHOOSE:EQUIPMENT|x,x`

## Parameters

-   x: Text (Equipment name)
-   x: TYPE=Text (Type Name)



<span id="chooseequipment"></span> \*\*\* New 5.10.1 RC3

What it does
------------

-   Will present a list of equipment, by name and/or type.
-   At least one (1) piece of equipment or equipment type must be
    designated for this tag to function properly.
-   There is no specific weapon chooser.

Example
-------

`CHOOSE:EQUIPMENT|TYPE=Goods`

A list of all equipment of type 'Goods'.

`CHOOSE:EQUIPMENT|TYPE=Martial|TYPE=Finessable`

A list of all equipment of types 'Martial' and 'Finessable'.

`CHOOSE:EQUIPMENT|TYPE=Natural|TYPE=Bludgeoning`

A list of all equipment of types 'Natural' and 'Bludgeoning'.

`CHOOSE:EQUIPMENT|TYPE=Alchemical|TYPE=Consumable`

A list of all equipment of types 'Alchemical' and 'Consumable'.

