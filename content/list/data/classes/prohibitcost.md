+++
date = "2016-08-01"
title = "PROHIBITCOST (Data: classes.lst)"
original_url = "/list/data/classes.html#prohibitcost"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "PROHIBITCOST"
    parent = "data_classes"
+++

## Status

None

## Syntax

`PROHIBITCOST:x`

## Parameters

-   x: Integer



<span id="prohibitcost"></span> \*\*\* Added 5.4

What it does
------------

Determines the redeemed value (against COST) of this school if selected
as prohibited. Allows a prohibited cost to be set independently of the
cost.

Optional tag. If PROHIBITCOST is not present in the SUBCLASS line the
value will default to COST. A value of 0 prevents this school from being
prohibited.

Example
-------

`PROHIBITCOST:2`

The subclass has a prohibited cost of 2.

Where it is used
----------------

Subclass Line.

