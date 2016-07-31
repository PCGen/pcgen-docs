+++
date = "2016-08-01"
title = "FUMBLERANGE (Data: equipment.lst)"
original_url = "list/data/equipment.html#fumblerange"
categories = [ "all-tag", "equipment-tag" ]
+++

## Status

None

## Syntax

`FUMBLERANGE:x`

## Parameters

-   x: Text (Equipment fumble range)



<span id="fumblerange"></span> \*\*\* Added 5.7.15

What it does
------------

This is text which indicates the equipments fumble or error range. This
tag may also be used in EQMOD lines. If an equipment item has EQMODs,
the FUMBLERANGE text from the EQMOD supersedes the text from the item
itself (EQMODs applied to the primary weapon head trumps text in EQMODs
applied to the secondary weapon head).

Example
-------

`FUMBLERANGE:1-3`

Indicates and error range of 1-3.

`FUMBLERANGE:Natural 1`

Indicates and error range of a natural 1.

