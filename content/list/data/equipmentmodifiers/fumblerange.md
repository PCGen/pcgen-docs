+++
date = "2016-08-01"
title = "FUMBLERANGE (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#fumblerange"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "FUMBLERANGE"
    parent = "data_equipmentmodifiers"
    identifier = "data_equipmentmodifiers_FUMBLERANGE"
+++

## Status

None

## Syntax

`FUMBLERANGE:x`

## Parameters

-   x: Text (Equipment fumble range)



<span id="fumblerange"></span> \*\*\* New 5.7.15

What it does
------------

This is text which indicates the equipments fumble or error range. This
tag may also be used in Equipment lines. If an equipment item has
EQMODs, the FUMBLERANGE text from the EQMOD supersedes the text from the
item itself (EQMODs applied to the primary weapon head trumps text in
EQMODs applied to the secondary weapon head).

Example
-------

`FUMBLERANGE:1-3`

Indicates and error range of 1-3.

`FUMBLERANGE:Natural 1`

Indicates and error range of a natural 1.

