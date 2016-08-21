+++
date = "2016-08-01"
title = "TOTALCOST (Data: starting_kits.lst)"
original_url = "list/data/startingkits.html#totalcost"
categories = [ "all-tag", "startingkits-tag" ]
+++

## Status

New 6.01.06

## Syntax

`TOTALCOST:x`

## Parameters

-   x: Formula (Cost)



What it does
------------

This sets a total monetary cost for kit. It overrides EQUIPBUY and
individual item costs but is affected by the buy rate selected on the
purchase tab. If a character cannot afford the TOTALCOST the kit will be
regarded as not qualified. It is used where a source provides a kit at a
specific cost.

Example
-------

`TOTALCOST:170`

The KIT costs 170gp for all gear.

`TOTALCOST:if(var("SIZE==3||SIZE==4"),5,10)`

The kit will cost 5 gp if the SIZE variable is 3 or 4, otherwise it will
cost 10 gp.

Where it is used
----------------

STARTPACK lines

