+++
date = "2016-08-01"
title = "ISDEFAULTSIZE (System: sizeAdjustment.lst)"
original_url = "/list/system/sizeadjustment.html#isdefaultsize"
categories = [ "all-tag", "sizeadjustment-tag" ]
[menu.main]
    name = "ISDEFAULTSIZE"
    parent = "system_sizeadjustment"
    identifier = "system_sizeadjustment_ISDEFAULTSIZE"
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="isdefaultsize"></span>

### ISDEFAULTSIZE

**Mandatory:** Marks which of the creature sizes is the default for the
game mode.

#### Syntax {#syntax-1}

`SIZENAME:size_1 → ISDEFAULTSIZE:Y` indicates that `size_1` **is** the
default size for the game mode.

`SIZENAME:size_2 → ISDEFAULTSIZE:N` indicates that `size_2` **is not**
the default size.

#### Example {#example-1}

`SIZENAME:Medium → ISDEFAULTSIZE:Y` makes `Medium` the default size for
this game mode.

#### Notes {#notes-1}

There must be one, and only one, size marked as the default size.

-   It is an error to have no size marked as the default size.
-   It is an error to have more than one default size.

If the `ISDEFAULTSIZE` tag is missing for a particular `SIZENAME` , then
`ISDEFAULTSIZE:N` is assumed.

