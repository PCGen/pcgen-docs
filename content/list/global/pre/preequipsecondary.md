+++
date = "2016-08-01"
title = "PREEQUIPSECONDARY (Global: PRErequisite)"
original_url = "list/global/pre.html#preequipsecondary"
categories = [ "all-tag", "pre-tag" ]
+++

## Status

None

## Syntax

`PREEQUIPSECONDARY:x,y,y`

## Parameters

-   x: Number (The number of items from the list that
    must be equipped in a secondary hand).
-   y: Text (The name of a piece of equipment - "%" may
    be used as a wildcard).
-   y: TYPE=Text (The type of a piece of equipment).
-   y: WIELDCATEGORY=Text (The wield category of
    a weapon).



What it does
------------

This is used to determine if a character has a particular item (usually
a weapon) equipped in a Secondary hand for the character. Typically has
a value of 1 for the Number, however can be more than one if can have
more than one Secondary hand.

Examples
--------

`PREEQUIPSECONDARY:1,Dagger`

Must have a dagger equipped in the secondary hand.

`PREEQUIPSECONDARY:1,Dagger%`

The "%" allows for items named Dagger (Masterwork), Dagger (Punching),
etc.

`PREEQUIPSECONDARY:1,TYPE=Slashing`

Must have some type of slashing weapon equipped in the secondary hand.

`PREEQUIPSECONDARY:1,WIELDCATEGORY=Light`

Must have a light weapon equipped in the secondary hand.

