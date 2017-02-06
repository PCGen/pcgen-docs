+++
date = "2016-08-01"
title = "STRING (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#string"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "STRING (Data: equipment_modifiers.lst)"
    parent = "equipmentmodifiers"
+++

## Status

None

## Syntax

`CHOOSE:STRING|x|x|y`

## Parameters

-   x: Text (Choice to be offered)
-   y: TITLE=Text (Chooser dialog title)



<span id="string"></span> \*\*\* Updated 5.13.8

What it does
------------

This will produce a list of the provided strings.

Example
-------

`CHOOSE:STRING|+1|+2|TITLE=Enhancement Bonus`

This will produce an "Enhancement Bonus" list consisting of "+1" and
"+2".

`CHOOSE:STRING|Undead|Constructs|Monkeys|TITLE=Biggest Irritant`

This will produce a list consisting of "Undead", "Constructs" and
"Monkeys".

