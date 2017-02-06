+++
date = "2016-08-01"
title = "STRING (Global: CHOOSE)"
original_url = "/list/global/choose.html#string"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "STRING (Global: CHOOSE)"
    parent = "choose"
+++

## Status

New 5.13.4

## Syntax

`CHOOSE:STRING|x|x`

## Parameters

-   x: Text (Choice to be offered)



What it does
------------

-   This will produce a list of the provided strings.
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

Example
-------

`CHOOSE:STRING|+1|+2`

This will produce a list consisting of "+1" and "+2".

`CHOOSE:STRING|Undead|Constructs|Monkeys`

This will produce a list consisting of "Undead", "Constructs" and
"Monkeys".

Ability, Domain, Feat, Race, and Template files.

