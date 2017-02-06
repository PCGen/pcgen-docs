+++
date = "2016-08-01"
title = "CONTAINS (Data: equipment.lst)"
original_url = "/list/data/equipment.html#contains"
categories = [ "all-tag", "equipment-tag" ]
[menu.main]
    name = "CONTAINS (Data: equipment.lst)"
    parent = "equipment"
+++

## Status

None

## Syntax

`CONTAINS:x|y=z`

## Parameters

-   x: Number (Weight held)
-   y: Text (Item type)
-   y: Total
-   z: Number (Quantity allowed)



<span class="status"><span id="contains"></span> \*\*\* Updated 5.14.0
</span>

What it does
------------

-   This tag is used to define how much, by weight and what type of
    object, a container can hold.
-   Any object with `CONTAINS` must also include a `TYPE:Container` tag
    for the `CONTAINS` tag to be activated.
-   The first parameter (x) is the maximum weight the container
    can hold.
    -   An asterisk (\*) means that the weight added doesn't change the
        weight of the container (e.g. a Bag of Holding).
    -   A number followed by a percentage (%) symbol before the quantity
        will reduce the total encumbrance weight of items in the
        container by the percentage specified.
    -   The name of the weight unit is defined in the game mode system
        files in the <span class="lstfile"> miscinfo.lst </span> file
        with the tag `WEIGHTUNITABBREV` .
-   The second parameter (y) identifies the type of items the container
    may hold.
    -   If there are no type's specified the container may hold anything
    -   Specific tags (Potions, Rings, Armor, etc) can be specified with
        a limit to how many can be in the container (e.g. Scroll Case)
    -   If specific tags are used the container may only hold the listed
        object types.
    -   A limit to the total number of things contained can be specified
        by setting a Total=x tag.
-   The third parameter (z) identifies the quantity allowed for the
    associated type of items.

**Note:** `UNLIM` may be used, in either (x) or (z), to indicate an
unlimited weight allowance for the container or the item type quantity.
If no value is provided for (z), `UNLIM` is assumed. PCGen's Data
Converter will remove `UNLIM` when converting a data file.

Examples
--------

`CONTAINS:500`

500 units of weight can fit in this container.

`CONTAINS:*500`

500 units of weight can fit in this container and this is not added to
the PCs carried weight.

`CONTAINS:50%50|Any=25`

Holds up to 25 items of up to 50 units of weight, but the total weight
contained is reduced 50%.

`CONTAINS:25%UNLIM|Any=100`

Holds up to 100 items no matter the weight, but total weight contained
is reduced 25%.

`CONTAINS:500|Potions=100`

500 units of weight can fit in this container, but only 100 potions fit.

`CONTAINS:UNLIM`

This container has an unlimited weight allowance.

`CONTAINS:UNLIM|Any=100`

Holds 100 things, no matter what the weight.

`CONTAINS:UNLIM|Total=10|Paper=10|Scroll=10`

Holds 10 papers or 10 scrolls, or any combination of these up to 10, no
matter what the weight.

