+++
date = "2016-08-01"
title = "ICON (Data: equipment.lst)"
original_url = "list/data/equipment.html#icon"
categories = [ "all-tag", "equipment-tag" ]
+++

## Status

Added 5.17.7

## Syntax

`ICON:x`

## Parameters

-   x: Text (file path)



What it does
------------

This occurs on an equipment line and sets the path to the icon to be
used for the equipment item. The path is relative to the pcgen install
folder. The same @, & and \* shortcuts as are used in PCC files may be
used in the path to specify where the path is relative to.

Example
-------

`ICON:@/d20ogl/srd35/icons/backpack.png`

The icon for this item will be d20ogl/srd35/icons/backpack.png relative
to the data directory.

