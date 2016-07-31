+++
date = "2016-08-01"
title = "MASTERBONUSRACE (Data: companion_mods.lst)"
original_url = "list/data/companionmodifiers.html#masterbonusrace"
categories = [ "all-tag", "companionmodifiers-tag" ]
+++

## Status

None

## Syntax

`MASTERBONUSRACE:x`

## Parameters




**Variables used (x):** Text (Race Name)

What it does
------------

-   The `MASTERBONUSRACE` tag is the first tag on a
    MASTERBONUSRACE line.
-   The MASTERBONUSRACE line is used to define the advantages that the
    master gains when having a particular race(s) as the given type
    of companion.
-   The tags following the `MASTERBONUSRACE` tag on the MASTERBONUSRACE
    line are granted to the master.
-   Valid tags on this line are `TYPE` , `BONUS` , `VFEAT` and the
    `ABILITY` tags.

Example
-------

`MASTERBONUSRACE:Bat`

Specifies what race the master has chosen (Bat) and the tag(s) following
it will give the master the familiar bonuses.

