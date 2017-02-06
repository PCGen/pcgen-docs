+++
date = "2016-08-01"
title = "PREPOINTBUYMETHOD (Global: PRErequisite)"
original_url = "/list/global/pre.html#prepointbuymethod"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREPOINTBUYMETHOD (Global: PRErequisite)"
    parent = "pre"
+++

## Status

Updated 5.13.12

## Syntax

`PREPOINTBUYMETHOD:x,y,y`

## Parameters

-   x: Number (Number of required point-buy methods)
-   y: Text (Pointbuy method)



What it does
------------

-   Sets a prerequisite based upon the saved method used by the
    point-buy system of stat determination.
-   **Note:** Only one (1) point-buy method is used at any given time so
    using a value greater then one is unecessary.

Examples
--------

`PREPOINTBUYMETHOD:1,Standard`

Sets a prerequisite of "Standard" for the point-buy saved method.

`PREPOINTBUYMETHOD:1,Standard,High-powered`

Sets a prerequisite of "Standard" or "High-powered" for the point-buy
saved method.

