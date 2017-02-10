+++
date = "2016-08-01"
title = "PREAPPLY (Global: PRErequisite)"
original_url = "/list/global/pre.html#preapply"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREAPPLY"
    parent = "global_pre"
+++

## Status

deprecated 6.1.1 - Remove for 6.4 - Use TEMPBONUS

## Syntax

`PREAPPLY:x,x`

## Parameters

-   x: ANYPC (Apply to any character).
-   x: PC (Apply to the character).
-   x: Text (A type name).



What it does
------------

-   Requires that the included qualifications be met by the target
    before the associated `BONUS` will be applied to that target.
-   `PREAPPLY` works **ONLY** at the end of a `BONUS` tag.
-   Bonuses with `PREAPPLY` tags will only appear in the *Temporary
    Bonuses Tab* .
-   Use a comma-delimiter (,) to indicate a logical **AND** , i.e. both
    conditions must be met.
-   Use a semi-colon delimiter (;) to indicate a logical **OR** , i.e.
    either condition must to be met.
-   All LST objects containing `BONUS` tags with `ANYPC` as the target
    of a `PREAPPLY` tag will always show up on the *Temporary Bonus
    Tab* .
-   Use of the `ANYPC` subtag allows for bonuses to be granted without
    the character needing to have added the containing object to his
    character, or to allow for conditional/situational bonuses on LST
    objects that have been added to the character.
-   LST objects that can include a `PREAPPLY:ANYPC` tag include:
    -   Spells that can be cast on any character.
    -   Abilities that contain conditional or situational bonuses.
    -   Feats that contain conditional or situational bonuses.
    -   Skills that contain conditional or situational bonuses.
    -   Templates that contain conditional or situational bonuses.
-   Spells with `PREAPPLY` tags with weapon types will be treated as
    containing `ANYPC` subtag and will appear in the *Temporary Bonuses
    Tab* with such bonuses applied only to a weapon that meets the type
    requirements specified.
-   See the documentation for the [Temporary Bonus
    Tab](/tabpages/players/inventory/inventorytempbonus.html) for more
    information on using this tag.

Examples
--------

`PREAPPLY:ANYPC`

This allows the bonus granted to be applied to any character.

`PREAPPLY:PC`

This allows the bonus granted to be applied to the PC to which the
granting LST object is attached.

`PREAPPLY:Ranged;Melee`

This allows the bonus granted to be applied to either ranged or melee
weapons.

`PREAPPLY:Weapon,Blunt`

This allows the bonus granted to be applied to blunt weapons only.

Example Conversion to TEMPBONUS tag
-----------------------------------

`BONUS:COMBAT|AC|2|PREAPPLY:PC` becomes `TEMPBONUS:PC|COMBAT|AC|2`

