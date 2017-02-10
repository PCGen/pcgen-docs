+++
date = "2016-08-01"
title = "WIELD (Data: equipment.lst)"
original_url = "/list/data/equipment.html#wield"
categories = [ "all-tag", "equipment-tag" ]
[menu.main]
    name = "WIELD"
    parent = "data_equipment"
+++

## Status

None

## Syntax

`WIELD:x`

## Parameters

-   x: Light (Weapon is Light)
-   x: OneHanded (Weapon can be wielded in one hand)
-   x: TwoHanded (Weapon requires both hands to be
    wielded effectively)



<span id="wield"></span> \*\*\* Added 5.5.2

What it does
------------

Sets the wield category of a weapon.

In 3.5 edition the rules for wielding a weapon are based on the size
category of the weapon and the size category of the PC. Each size
category difference between the weapon and PC changes the effective
wield category by one step. Thus a Large sized Longsword, a 'OneHanded'
weapon, is effectively wield category 'TwoHanded' for a Medium sized PC.

Example
-------

`WIELD:TwoHanded`

Weapon must be wielded with two hands.

Where it is used
----------------

Equipment files in melee weapon lines.

