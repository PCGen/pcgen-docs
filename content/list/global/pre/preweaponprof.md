+++
date = "2016-08-01"
title = "PREWEAPONPROF (Global: PRErequisite)"
original_url = "/list/global/pre.html#preweaponprof"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREWEAPONPROF"
    parent = "global_pre"
    identifier = "global_pre_PREWEAPONPROF"
+++

## Status

Updated 5.13.0

## Syntax

`PREWEAPONPROF:x,y,y`

## Parameters

-   x: Number (Number of matching proficiencies).
-   y: Text (Weapon proficiency name).
-   y: TYPE.Text (Weapon Proficiency type).
-   y: DEITYWEAPON (Deities favored weapon).



What it does
------------

-   Sets requirements based upon weapon proficiencies held.
-   Though types can be used within this tag, their use can be tricky
    and can sometiime produce unexpected or unwanted results.

Examples
--------

`PREWEAPONPROF:2,Kama,Katana`

Character must have proficiency with both the "Kama" and the "Katana".

`PREWEAPONPROF:1,TYPE.Exotic`

Character must have a weapon proficiency of type "Exotic".

`PREWEAPONPROF:1,TYPE.Martial,Chain (Spiked)`

Character must have either a weapon proficiency of type "Martial" or
proficiency with "Chain (Spiked)".

`PREWEAPONPROF:1,DEITYWEAPON`

Character must have proficiency with one of the chosen deity's favored
weapons.

