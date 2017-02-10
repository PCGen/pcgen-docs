+++
date = "2016-08-01"
title = "SIZE (Data: races.lst)"
original_url = "/list/data/races.html#size"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "SIZE"
    parent = "data_races"
    identifier = "data_races_SIZE"
+++

## Status

None

## Syntax

`SIZE:x`

## Parameters

-   x: Text (F,D,T,S,M,L,H,G,C)



<span id="size"></span> \*\*\* Updated 5.12 RC3

What it does
------------

-   Determines the size of the Race. (F=Fine, D=Diminutive, T=Tiny,
    S=Small, M=Medium, L=Large, H=Huge, G=Gargantuan, C=Colossal). Size
    is used in determining to-hit, AC, and affects some skills.
-   The size designations, including abbreviations, are dependant upon
    the gamemode used and may be redefined in the
    sizeadjustments.lst file.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `SIZE` tag, the data included in a new `SIZE` tag will
    overwrite the existing tag data.

**Special Sizes:**

-   SIZE:P - Mode: RSRD (35e) - Colossal+ - Restricted to only dragons.
-   SIZE:C - Mode: Spycraft 2 - Vast - .

Example
-------

`SIZE:M`

The race is of Medium size.

**.MOD Example:**

Initial Race: `<race name> <tab> SIZE:M`

Modified By: `<race name>.MOD <tab> SIZE:L`

Is Equivalent To: `<race name> <tab> SIZE:L`

The creatue is "Large".

