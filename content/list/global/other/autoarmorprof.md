+++
date = "2016-08-01"
title = "AUTOARMORPROF (Global: OTHER)"
original_url = "/list/global/other.html#autoarmorprof"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "AUTOARMORPROF"
    parent = "global_other"
+++

## Status

Updated 5.17.11

## Syntax

`AUTO:ARMORPROF|x|x`

## Parameters

-   x: Text (Armor name)
-   x: ARMORTYPE=Text (Armor type)



What it does
------------

-   This is a pipe-delimited (|) list of armor, by name or by armor
    type, that are granted as free armor proficiencies.
-   When including the `ARMORTYPE=` sub-tag you may use a
    period-delimted (.) list of armor types. This will grant the
    character proficiency with armor that meet all of the listed
    armor types.
-   PRExxx tags are allowed with this tag and use the pipe-delimited (|)
    syntax.

Examples
--------

`AUTO:ARMORPROF|ARMORTYPE=Light`

All Light armors are given as free armor proficiencies.

`AUTO:ARMORPROF|Leather`

Leather armor is given as a free armor proficiency.

`AUTO:ARMORPROF|ARMORTYPE=Light|ARMORTYPE=Medium`

Light and Medium Armor is given as a free armor proficiency.

`AUTO:ARMORPROF|Dwarven Plate|PRERACE:1,Dwarf`

Dwarven Plate is given as a free armor proficiency if the character is a
Dwarf.

