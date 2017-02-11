+++
date = "2016-08-01"
title = "LOCATION (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#location"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "LOCATION"
    parent = "data_startingkits"
    identifier = "data_startingkits_LOCATION"
+++

## Status

New 5.9.3

## Syntax

`LOCATION:x,x`

## Parameters

-   x: Text (Location to be equipped)



What it does
------------

-   LOCATION is used in GEAR lines to specify the location the item will
    be equipped to. If an item is of a TYPE with a specific slot then
    setting it to Equipped will equip it there. Only weapons need more
    specific settings.
-   The following are valid "Locations":
    -   Both Hands
    -   Carried
    -   Double Weapon
    -   Equipped
    -   Natural-Primary
    -   Natural-Secondary
    -   Not Carried
    -   Primary Hand
    -   Secondary Hand
    -   Shield
    -   Two Weapons

Example
-------

`GEAR:Morningstar <tab> LOCATION:Primary Hand`

Equips the Morningstar to the Primary Hand slot.

`GEAR:Leather <tab> LOCATION:Equipped`

Equips the Leather armor to the Armor slot.

`GEAR:Shield (Light/Wood) <tab> LOCATION:Equipped`

Equips the Shield to the Shield slot.

`GEAR:Javelin <tab> LOCATION:Carried`

Equips the Javelin to Carried.

Where it is used
----------------

GEAR lines

