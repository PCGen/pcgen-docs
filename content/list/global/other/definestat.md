+++
date = "2016-08-01"
title = "DEFINESTAT (Global: OTHER)"
original_url = "/list/global/other.html#definestat"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "DEFINESTAT"
    parent = "global_other"
+++

## Status

New 6.01.03

## Syntax

`DEFINESTAT:x|y|z`

## Parameters

-   x: LOCK
-   x: UNLOCK
-   x: NONSTAT
-   x: STAT
-   x: MINVALUE
-   x: MAXVALUE
-   y: Text (Stat defined in loaded gameMode)
-   z: Number or Formula



What it does
------------

-   This tag will lock or unlock the value of an ability score.
    -   Using `LOCK` will lock the designated ability score (y) to the
        value (z) regardless of any other bonuses to that ability score
        except for those applied by the
        [BONUS:LOCKEDSTAT](/list/global/bonus/lockedstat.html) tag.
    -   Using `UNLOCK` will unlock the designated ability score (y) that
        has previously been locked.
    -   The `UNLOCK` sub-tag will not affect an ability score that has
        been designated as a "nonstat". (see `NONSTAT` below).
-   This tag will also change an ability score from a stat to a nonstat.
    -   Ability scores are by default designated as "stats" when
        initialized during character creation.
    -   Using `NONSTAT` will change an ability score to a non-stat,
        causing it to be shown as an asterisk (\*) on output sheets and
        prohibiting any bonuses from being applied.
    -   Using `STAT` will change an ability score that has been
        previously designated as a nonstat back to a stat without
        affecting its locked/unlocked state.
-   Using `MINVALUE` defines the minimum value (z) for the designated
    ability score (y).
-   Using `MAXVALUE` defines the maximum value (z) for the designated
    ability score (y).

Example
-------

`DEFINESTAT:LOCK|INT|10`

Locks the stat "Intelligence" to 10.

`DEFINESTAT:UNLOCK|INT`

Unlocks previously locked stat "Intelligence".

`DEFINESTAT:NONSTAT|INT`

Changes the ability score "Intelligence" to a non-stat, causing it to
appear on the output sheet as an asterisk.

`DEFINESTAT:STAT|INT`

Changes the ability score "Intelligence" that has been previously
changed to a non-stat back to a normal stat.

`DEFINESTAT:MINVALUE|INT|3`

The creature cannot have an "Intelligence" less than 3.

`DEFINESTAT:MAXVALUE|INT|10`

The creature cannot have an "Intelligence" more than 10.

