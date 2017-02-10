+++
date = "2016-08-01"
title = "FEATPOOL (Global: BONUS)"
original_url = "/list/global/bonus.html#featpool"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "FEATPOOL"
    parent = "global_bonus"
    identifier = "global_bonus_FEATPOOL"
+++

## Status

New 5.7.6

## Syntax

`BONUS:FEAT|POOL|x`

## Parameters

-   x: Number, variable or formula (Number to add or
    subtract from the feat pool)



### FEATPOOL

-   6.05.04 (July 2015): JIRA
    [NEWTAG-477](http://jira.pcgen.org/browse/NEWTAG-477) / Github [PR
    \#380](https://github.com/PCGen/pcgen/pull/380)
-   -   The `FEATPOOL` tag is deprecated. Use
        [`ABILITYPOOL`](/list/global/bonus/abilitypool.html) instead.
    -   All `FEAT` tags have been **deprecated** and replaced by the
        `ABILITY` system, which is more general. The `ABILITY` system
        can model feats, racial features, class features, traits, flaws,
        temporary bonuses, and so on, all using a common format.

<div class="deprecated">

What it Does
------------

Modifies the character's feat pool total. Can be qualified by PRExxx
tags and TYPE tags like other BONUS tags.

Example
-------

`BONUS:FEAT|POOL|1`

Increases the feat pool by one.

`BONUS:FEAT|POOL|1|TYPE=Enhancement`

Increases the feat pool by one and will not stack with other
BONUS:FEAT|POOL tags with TYPE=Enhancement.

`BONUS:FEAT|POOL|-1|PREFEAT:1,Alertness`

Decreases the feat pool by one if the character has the feat Alertness.

</div>

