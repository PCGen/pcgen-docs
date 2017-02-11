+++
date = "2016-08-01"
title = "BONUSPPCOST (Data: spells.lst)"
original_url = "/list/data/spells.html#bonusppcost"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "BONUSPPCOST"
    parent = "data_spells"
    identifier = "data_spells_BONUSPPCOST"
+++

## Status

NEW 5.10.1

## Syntax

`BONUS:PPCOST|x|y`

## Parameters

-   x: Text (Spell Name)
-   y: Number (Power Points)



What it does
------------

It is possible to scale some spells to increase range, duration, damage,
etc. Scaling uses more PPs. For every one point in extra power applied
to the spell the spell's Effective Caster Level for damage purpose is
raised 1 level. Maximum level applied is equal to the Caster's current
level.

Example
-------

`BONUS:PPCOST|Blade Barrier|3`

It costs a Clr9/Good9/War9 11 PP to launch a Blade Barrier for 6d6
damage. By putting in 3 more points, the Effective Caster Level is 9d6
for a total of 14 PP. The maximum extra PP is 3 for this example. Damage
can not be raised over the Caster's actual level.

`BONUS:PPCOST|Lightning Bolt|2`

It costs a Sor/Wiz 9 5 PP to launch a Lightning Bolt for 3d6 damage. By
putting in 2 more points, the Effective Caster Level is 5d6 damage for a
total of 7 PP. The maximum extra PP is 7 for this example getting the
maximum of 10d6 damage.

