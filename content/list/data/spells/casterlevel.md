+++
date = "2016-08-01"
title = "CASTERLEVEL (Data: spells.lst)"
original_url = "list/data/spells.html#casterlevel"
categories = [ "all-tag", "spells-tag" ]
+++

## Status

Updated 5.13.8

## Syntax

`CASTERLEVEL (Spell
Variable)`

## Parameters




What it does
------------

-   CASTERLEVEL is a special variable for use within
    [DESC](/list/data/spells.html#desc) ,
    [DURATION](/list/data/spells/duration.html) and
    [TARGETAREA](/list/data/spells/targetarea.html) tags.
    -   When these tags encounter text in parenthesis, they treat the
        text as a formula and replace it with the result of evaluating
        the formula.
    -   When used inside parenthesis in these tags, `CASTERLEVEL`
        returns the caster level of the class which grants the spell.
-   The value of `CASTERLEVEL` depends mostly on the "Class" granting
    the spell, but can be affected by "Race" or by other attributes of
    the spell (e.g. School, Descriptor, etc.).
-   `CASTERLEVEL` can be adjusted using the
    [BONUS:CASTERLEVEL](/list/global/bonus/casterlevel.html) tag. In
    some cases where division and multiplication are used it is
    recommended that the
    [floor()](/list/global/formulas.html#truncation) function
    be applied.

Example
-------

`DESC:Electricity deals (CASTERLEVEL)d6 damage`

If the caster level is 2, the output reads:Electricity deals 2d6 damage.

`DURATION:((CASTERLEVEL/3)+1) rounds`

If the caster level is 6, the output reads:DURATION:3 rounds

`TARGETAREA:(floor((CASTERLEVEL/2)*5)+25)`

If the caster level is 7, the output reads:TARGETAREA:40 (Note that if
floor() were not used formula would return 42).

`DURATION:(CASTERLEVEL) rounds`

If the caster level is 3, the output reads:DURATION:3 rounds

`DESC:Random damage in area during duration, plus (CASTERLEVEL)d4 damage`

If the caster level is 3, output reads:DESC:Random damage in area during
duration, plus 3d4 damage

