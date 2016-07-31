+++
date = "2016-08-01"
title = "TEMPBONUS (Global: BONUS)"
original_url = "list/global/bonus.html#tempbonus"
categories = [ "all-tag", "bonus-tag" ]
+++

## Status

New 6.01.01

## Syntax

`TEMPBONUS:x,x|y|z`

## Parameters

-   x: PC (Target)
-   x: ANYPC (Target)
-   x: EQ (Target)
-   y: Text (Equipment types)
-   z: Text (Bonus subtoken with appropriate syntax
    and parameters)



What it Does
------------

-   Provides a temporary bonus that can be applied to the
    applicable target.
-   Temporary bonuses are applied to characters/equipment on the
    [Temporary Bonus
    Tab](/tabpages/players/inventory/inventorytempbonus.html) .
-   The temporary bonus includes the following targets:
    -   `PC` - The temporary bonus can only be applied to a character
        that has been 'granted' the LST object that contains the
        `TEMPBONUS` tag.
    -   `ANYPC` - The temporary bonus can be applied to any character
        whether the LST object containing the `TEMPBONUS` tag has been
        granted to the character or not.
    -   `EQ` - The temporary bonus can only be applied to equipment of
        the type identified by the (y) parameter.
-   The equipment type, variable (y), is used only when the target of
    the bonus is `EQ` , and in this case it is required.
-   The bonus subtoken syntax and parameters are as per the
    appropriate bonus. (See standard `BONUS` tag documentation above.
-   As with the standard bonus tags, the `TEMPBONUS` tag can take `TYPE`
    and `PRExxx` tags.

Example
-------

`TEMPBONUS:PC|COMBAT|AC|2`

Increases armor class by two for the character granted the LST object
containing the `TEMPBONUS` . This is equivalent to `BONUS:COMBAT|AC|2`
but is applied as a temporary bonus.

`TEMPBONUS:ANYPC|CHECKS|Fortitude,Reflex|1`

Adds one to "Fortitude" and "Reflex" saves for any character. This is
equivalent to `BONUS:CHECKS|Fortitude,Reflex|1` but is applied as a
temporary bonus.

`TEMPBONUS:EQ|TwoHanded|WEAPON|DAMAGE|1`

Adds one to the damage done by the two-handed weapon on which the bonus
is applied. This is equivalent to `BONUS:WEAPON|DAMAGE|1` but is applied
as a temporary bonus.

Example Conversion from PREAPPLY to TEMPBONUS
---------------------------------------------

`BONUS:COMBAT|AC|2|PREAPPLY:PC` becomes `TEMPBONUS:PC|COMBAT|AC|2`

Where it is Used
----------------

Ability, Class, Feat, Equipment, Skill, Spell and Template objects.

