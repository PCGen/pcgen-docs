+++
date = "2016-08-01"
title = "BONUSLOADMULT (System: sizeAdjustment.lst)"
original_url = "/list/system/sizeadjustment.html#bonusloadmult"
categories = [ "all-tag", "sizeadjustment-tag" ]
[menu.main]
    name = "BONUSLOADMULT"
    parent = "system_sizeadjustment"
    identifier = "system_sizeadjustment_BONUSLOADMULT"
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="bonusloadmult"></span>

### BONUS:LOADMULT

Adds to the `SIZEMULT` value as defined in the `load.lst` game mode
file.

Mostly, the rules for "Large creatures can carry twice as much weight"
[and so
on](http://www.d20srd.org/srd/carryingCapacity.htm#biggerandSmallerCreatures)
are implemented in `load.lst` . The `BONUS:LOADMULT` tag is used to
implement rules for creatures with four legs having greater
load-carrying capacity.

Only works in `sizeAdjustment.lst`.

#### Status {#status-6}

New in 5.10.1

#### Syntax {#syntax-8}

`BONUS:LOADMULT|TYPE=SIZE|sizemult_modifier`

-   `sizemult_modifier` is a number. This number is added to the
    `SIZEMULT` in the `load.lst` file to determine the "effective"
    carrying capacity multiplier, relative to a normal sized creature.

#### Examples {#examples-3}

-   `SIZENAME:H  →  BONUS:LOADMULT|TYPE=SIZE|2`

Increases the creature's carrying capacity by one multiple of the normal
carrying capacity. This adds with the multiplier already defined for the
creature's size category, in `load.lst` .

For example, in DnD 3.5e, a huge-size creature can already carry four
times the load of a medium-size creature. This is defined by the code
`SIZEMULT:H|4` in `load.lst` .

The above `BONUS:LOADMULT|...|2` increases this by a further two
multiples of the medium-size creature's carrying capacity, to a total of
six times.

-   `SIZENAME:H  →  BONUS:LOADMULT|TYPE=SIZE|2|PRELEGSGTEQ:4`

Like the above, but will only apply if the creature has at least four
legs.

