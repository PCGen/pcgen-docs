+++
date = "2016-08-01"
title = "EQUIPBUY (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#equipbuy"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "EQUIPBUY (Data: starting_kits.lst)"
    parent = "startingkits"
+++

## Status

New 5.8

## Syntax

`EQUIPBUY:x`

## Parameters

-   x: Number (Percentage)



What it does
------------

This sets the percentage that the total cost of all the gear in the kit
is discounted (or inflated by). If set to 0 the gear is granted for
free.

Example
-------

`EQUIPBUY:0`

The gear granted by the KIT is free.

`EQUIPBUY:50`

The gear granted by the KIT is granted for half the normal cost.

`EQUIPBUY:200`

The gear granted by the KIT is granted for twice the normal cost.

Where it is used
----------------

STARTPACK lines

