+++
date = "2016-08-01"
title = "PAGEUSAGE (Data: equipment.lst)"
original_url = "list/data/equipment.html#pageusage"
categories = [ "all-tag", "equipment-tag" ]
+++

## Status

None

## Syntax

`PAGEUSAGE:x`

## Parameters

-   x: Formula (Number of pages each spell will use)



<span id="pageusage"></span> \*\*\* Added 5.9.6

What it does
------------

Defines the how many pages of the spellbook each spell would use. The
variable SPELLLEVEL can be used to make calculations based on the
spell's level. Any equipment item with TYPE:Spellbook will appear in the
Spellbook sub-tab of the Spells Tab.

Example
-------

`PAGEUSAGE:max(SPELLLEVEL*2,1)`

Each spell will use 2 pages per level (3.0 standard spellbook).

`PAGEUSAGE:1`

Each spell will use a single page (Blessed Book).

