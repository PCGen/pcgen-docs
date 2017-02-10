+++
date = "2016-08-01"
title = "PREEQUIPPRIMARY (Global: PRErequisite)"
original_url = "/list/global/pre.html#preequipprimary"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREEQUIPPRIMARY"
    parent = "global_pre"
+++

## Status

None

## Syntax

`PREEQUIPPRIMARY:x,y,y`

## Parameters

-   x: Number (The number of items from the list that
    must be equipped in a primary hand).
-   y: Text (The name of a piece of equipment - "%" may
    be used as a wild-card).
-   y: TYPE=Text (The type of a piece of equipment).
-   y: WIELDCATEGORY=Text (The wield category of
    a weapon).



What it does
------------

This is used to determine if a character has a particular item (usually
a weapon) equipped in a Primary hand for the character. Typically has a
value of 1 for the Number, however can be more than one if can have more
than one Primary hand.

Examples
--------

`PREEQUIPPRIMARY:1,Dagger`

Must have a dagger equipped in the primary hand.

`PREEQUIPPRIMARY:1,Dagger%`

The "%" allows for items named Dagger (Masterwork), Dagger (Punching),
etc.

`PREEQUIPPRIMARY:1,TYPE=Slashing`

Must have some type of slashing weapon equipped in the primary hand.

`PREEQUIPPRIMARY:1,WIELDCATEGORY=OneHanded`

Must have a one handed weapon equipped in the primary hand.

