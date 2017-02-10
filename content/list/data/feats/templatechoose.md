+++
date = "2016-08-01"
title = "TEMPLATECHOOSE (Data: feats.lst)"
original_url = "/list/data/feats.html#templatechoose"
categories = [ "all-tag", "feats-tag" ]
[menu.main]
    name = "TEMPLATECHOOSE"
    parent = "data_feats"
+++

## Status

None

## Syntax

`TEMPLATE:CHOOSE:x|x`

## Parameters

-   x: Text (Template Name)



What it does
------------

-   Will present a popup window of the choices provided in the
    pipe-delimited (|) list, allowing the user to pick ONE from
    the list.
-   Multiple `TEMPLATE:CHOOSE` tags can be used in the same LST object
    but doing so can cause unintended results.

Example
-------

`TEMPLATE:CHOOSE:Celestial|Outsider`

The feat allows the selections of either the "Celestial" or "Outsider"
template.

