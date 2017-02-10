+++
date = "2016-08-01"
title = "EQUIP (Global: ADD)"
original_url = "/list/global/add.html#equip"
categories = [ "all-tag", "add-tag" ]
[menu.main]
    name = "EQUIP"
    parent = "global_add"
    identifier = "global_add_EQUIP"
+++

## Status

New 5.11.11

## Syntax

`ADD:EQUIP|x|y,y`

## Parameters

-   x: Number, Variable or Formula (Number of
    choices granted. Optional)
-   y: Text (Name of item)
-   y: TYPE=Text (Equiment type)



What it does
------------

-   Will add a number (x) of equipment items from the presented list (y)
    to the character.
-   The equipment list is a comma-delimited (",") list.
-   If the count (x) is not used, one item to be added is assumed.

Example
-------

`ADD:EQUIP|1|Torch,Lantern`

Add one of either a "Torch" or a "Lantern" to the character.

`ADD:EQUIP|Blastpowder (10)`

Add one of "Blastpowder (10)" to the character.

`ADD:EQUIP|2|Synchronicity Watch,Secret Pockets,Daylight Flares`

Add two of "Synchronicity Watch", "Secret Pockets" or "Daylight Flares"
to the character.

`ADD:EQUIP|Dagger (Sarishan Steel)`

Add one of "Sarishan Steel Dagger" to the character.

`ADD:EQUIP|TYPE=Thrown`

Add one piece of equipment of type "Thrown" to the character.

