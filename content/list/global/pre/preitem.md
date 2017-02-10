+++
date = "2016-08-01"
title = "PREITEM (Global: PRErequisite)"
original_url = "/list/global/pre.html#preitem"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREITEM"
    parent = "global_pre"
    identifier = "global_pre_PREITEM"
+++

## Status

None

## Syntax

`PREITEM:x,y,y`

## Parameters

-   x: Number (The number of items a character
    must possess).
-   y: Text (The name of an item a character must
    possess - "%" may be used as a wildcard).
-   y: TYPE=Text (The type of an item the character
    must possess).



What it does
------------

Sets requirements for items a character must possess.

TYPE.xxx for reference, TYPE=xxx for assignment.

Examples
--------

`PREITEM:1,Sword (Long),Sword (Short)`

Character must possess either a "long sword" or a "short sword".

`PREITEM:2,TYPE=Armor,TYPE=Armor`

Character must possess two sets of armor.

`PREITEM:1,TYPE=Natural`

Character must possess one natural item.

