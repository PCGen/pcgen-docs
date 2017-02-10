+++
date = "2016-08-01"
title = "LEVEL (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#level"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "LEVEL"
    parent = "data_startingkits"
    identifier = "data_startingkits_LEVEL"
+++

## Status

New 5.9.3

## Syntax

`LEVEL:x`

## Parameters

-   x: Number (Levels to add)



What it does
------------

-   Grants the character the number of class levels indicated if they
    can legally attain them.
-   Must be used with the `CLASS` tag.

Examples
--------

`CLASS:Warrior <tab> LEVEL:2`

Would grant the character two levels of the Warrior class.

`CLASS:Fighter <tab> LEVEL:4 <tab> PRECLASS:1,Fighter=1`

Would grant four levels of Fighter if the character has at least one
level in Fighter already.

Where it is Used
----------------

CLASS line

