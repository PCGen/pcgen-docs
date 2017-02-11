+++
date = "2016-08-01"
title = "SORTKEY (Global: OTHER)"
original_url = "/list/global/other.html#sortkey"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "SORTKEY"
    parent = "global_other"
    identifier = "global_other_SORTKEY"
+++

## Status

New 5.17.4

## Syntax

`SORTKEY:x`

## Parameters

-   x: Text (Alpha Numeric)



What it does
------------

-   This tag provides a generic text field by which LST objects can
    be sorted.
-   **SORTKEY** can be modified with the
    [MOD](/list/global/other/mod.html) tag.

**Note:** When sorting lists of objects, PCGen will sort by **SORTKEY**
, **OUTPUTNAME** then LST Name (e.g. "Enlarge Spell", "Quicken Spell",
etc), in that order. Sorts order is 0-9, A-Z.

Example
-------

`Enlarge Spell<tab>SORTKEY:Metamagic~Enlarge Spell`

`Quicken Spell<tab>SORTKEY:11-MetaMagic~Quicken Spell`

`Early Feat<tab>SORTKEY:Z-Me last`

Would Display as

Quicken Spell

Enlarge Spell

Early Feat

