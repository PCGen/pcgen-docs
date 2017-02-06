+++
date = "2016-08-01"
title = "FORMATCAT (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#formatcat"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "FORMATCAT (Data: equipment_modifiers.lst)"
    parent = "equipmentmodifiers"
+++

## Status

None

## Syntax

`FORMATCAT:x`

## Parameters

-   x: FRONT
-   x: MIDDLE
-   x: PARENS



<span id="formatcat"></span> \*\*\* New 5.11.0

What it does
------------

Defines how the equipment modifier's name will be displayed when an
equipment item name is being automatically generated. The valid values
and their actions are listed below:

-   FORMATCAT:FRONT - The eqmod name appears before the base equipment
    item name.
-   FORMATCAT:MIDDLE - The eqmod name appears after the base equipment
    item name but before the parenthesis.
-   FORMATCAT:PARENS - (Default) The eqmod name appears in brackets
    after the base equipment item name.

Example
-------

`Masterwork[tab]FORMATCAT:PARENS[tab]NAMEOPT:TEXT=MW`

when applied to a battleaxe would give battleaxe (MW)

`MAGIC_PLUS_1[tab]FORMATCAT:FRONT[tab]NAMEOPT:TEXT=+1`

when applied to a battleaxe would give +1 battleaxe

`MAGIC_PLUS_1[tab]FORMATCAT:MIDDLE[tab]NAMEOPT:TEXT=+1`

when applied to a battleaxe would give battleaxe +1

