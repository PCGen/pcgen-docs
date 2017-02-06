+++
date = "2016-08-01"
title = "CLASS (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#class"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "CLASS (Data: starting_kits.lst)"
    parent = "startingkits"
+++

## Status

New 5.9.3

## Syntax

`CLASS:x`

## Parameters

-   x: Text (Class name)



What it does
------------

-   Grants the character the specified class.
-   Used in conjunction with the `LEVEL` tag.

Examples
--------

`CLASS:Warrior <tab> LEVEL:2`

Would grant the character two levels of the Warrior class.

`CLASS:Fighter <tab> LEVEL:4 <tab> PRECLASS:1,Fighter=1`

Would grant four levels of Fighter if the character has at least one
level in Fighter already.

