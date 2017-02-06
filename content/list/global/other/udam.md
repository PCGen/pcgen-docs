+++
date = "2016-08-01"
title = "UDAM (Global: OTHER)"
original_url = "/list/global/other.html#udam"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "UDAM (Global: OTHER)"
    parent = "other"
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="udam"></span>

### UDAM

Sets the character's unarmed damage.

#### Status:

-   6.05.04 - JIRA issue
    [CODE-2866](http://jira.pcgen.org/browse/CODE-2866) / Github [PR
    \#385](https://github.com/PCGen/pcgen/pull/385)
    -   The 'damage by size category' syntax, with multiple arguments,
        now takes as many arguments as there are size categories in the
        `sizeAdjustment.lst` . *Typically* this is nine arguments.
        (Formerly took *exactly* nine arguments, ignoring
        `sizeAdjustment.lst` .)

#### Syntax

-   `UDAM:XdY`
    -   Sets the character's unarmed attack damage to `XdY` regardless
        of the character's current size.
-   `UDAM:XdY,XdY, ... ,XdY`
    -   Sets the character's unarmed attack damage by size.
    -   The arguments `XdY` are in ascending order of size.
    -   The number of arguments `XdY` must match the number of sizes
        listed in the game mode's `sizeAdjustment.lst` .
    -   For the `35e` game mode, there are nine sizes - *fine,
        diminutive, tiny, small, medium, large, huge, gargantuan,
        colossal, colossal+* .

#### Examples

1.  `UDAM:1d3` - sets un-armed damage to be `1d3` , no matter what size
    the creature is.
2.  `UDAM:1,1d2,1d3,1d4,1d6,1d8,1d10,1d12,2d8` - sets a damage
    progression for nine creature sizes, increasing from `1` point at
    the smallest size, to `2d8` at the largest size.


