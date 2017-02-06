+++
date = "2016-08-01"
title = "BASEITEM (Data: equipment.lst)"
original_url = "/list/data/equipment.html#baseitem"
categories = [ "all-tag", "equipment-tag" ]
[menu.main]
    name = "BASEITEM (Data: equipment.lst)"
    parent = "equipment"
+++

## Status

None

## Syntax

`BASEITEM:x`

## Parameters

-   x: Text (name of base item)



What it does
------------

-   This tag allows the creation of a new specific item based upon an
    existing item.
-   `BASEITEM` must be used in conjunction with the `EQMOD` tag.
-   Eqmods listed in the `EQMOD` tag are applied to the base item prior
    to the application of any other included tags.

NOTE: This tag will not copy any of the base item's existing tags so you
will need to add them yourself. The `.COPY` tag will perform this same
function but will copy all tags to the new item, verbatim, prior to
adding any new tags. (See [.COPY](/list/global/other/copy.html) docs)

Example
-------

> `Davril's Longsword <tab> BONUS:COMBAT|DAMAGE,TOHIT|2 <tab> BASEITEM:Longsword <tab> EQMOD:BANE_M|Undead.HOLY_M.KEEN`

Creates a piece of equipment called "Davril's Longsword" that is a +2
weapon. The SPROPS and effects from the equipment modifiers "Bane
Undead", "Holy" and "Keen" will appear in the attack numbers and special
properties as appropriate.

