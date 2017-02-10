+++
date = "2016-08-01"
title = "WEAPONBONUS (Data: classes.lst)"
original_url = "/list/data/classes.html#weaponbonus"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "WEAPONBONUS"
    parent = "data_classes"
+++

## Status

None

## Syntax

`WEAPONBONUS:x|x`

## Parameters

-   x: Text (Weapon Proficiency Name)
-   x: TYPE.Text (Weapon Type)



<span id="weaponbonus"></span> \*\*\* Updated 5.7.12

What it does
------------

-   This is a pipe-delimited (|) list of weapons or weapon types that
    are granted to the class as a choice of ONE of the listed weapons.
-   This tag does not use a CHOOSE pop-up to make a selection. You nust
    use the "Lang, Weapon, and SA" dialog found on the "Summary" tab.

Example
-------

`WEAPONBONUS:Dagger|Staff|Club|Mace|Sword (Short)|Shortbow (Composite)`

The class can choose from a weapon proficiency from "Dagger", "Staff",
"Club", "Mace", "Sword (Short)" or "Shortbow (Composite)".

`WEAPONBONUS:TYPE.Simple`

The class receives bonus proficiency in any one Simple weapon.

Where it is used
----------------

Class Level Line.

